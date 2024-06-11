Purpose: Write up a spec for cleaning up the logging system.

# Discussion

Reiner pointed out that his logs are several megabytes a day, with
Autoplot spewing out information useless to him, and actually no longer
useful to the developers. Java Logging is used half-heartedly throughout
the code, which is a system that lets you control how much of any
channel's information you want to here. The advantage of logging is you
can turn off the debug messages you need now and again to figure out
what's going on. The disadvantage is that it's difficult to use logging
effectively.

Reiner's complaints inspire me to go and clean all this up. Also, I've
recently learned how to add breakpoints to print debug messages, so this
reduces the need for System.err.println use. This is a document that
outlines how loggers will be configured so that they are used
consistently throughout the system.

See: <https://sourceforge.net/p/autoplot/bugs/913/> "autoplot logging is
verbose and inconsistent" and
<https://sourceforge.net/p/autoplot/bugs/2041/> "revisit Autoplot
logging"

# Logger top-level hierarchy

Note that logging is hierarchical. "das2" will include all the messages
of "das2.graph"

**das2** messages from the das2 graphics subsystem. This has a developed
namespace and I wouldn't want to mess with it.

**qdataset** messages with data handling. data operations.

**qstream** messages having to do with qstream formatting and parsing,
filtering

**datum** parsing and formatting. math.

**apdss** autoplot data source messages

**autoplot** autoplot application, applet, testing

**jython** jython

**jython.editor** having to do with completion, etc.

**console.stdout** when the console is visible, stdout messages are
handled via this logger

**console.stderr** when the console is visible, stderr messages are
handled via this logger

# Other loggers added

**autoplot.dom** having to do with loading and saving state

**autoplot.bookmarks** bookmarks system

**autoplot.pngwalk** pngwalk application

**autoplot.tsb** time series browse

**apdss.ascii** ascii datasource

**apdss.csv** csv datasource

**apdss.cdfjava** java cdf datasource

**apdss.html** html tables datasource

**apdss.jyds** Jython Data Source.

**apdss.dss** data set selector GUI

**apdss.agg** data source aggregator

**apdss.uri** data set URIs and registry

**qdataset.ascii** ascii parsing, which is done within the qdataset
package.

# LoggerManager

Ed came up with a nice idea for keeping track of loggers. The problem is
there's no way to discover loggers. So we use
org.das2.util.LoggerManager.getLogger("name") instead of just
Logger.getLogger("name"). The LoggerManager keeps track of all the
loggers it's accessed. Note too that there are two of these. Presently
the two projects dasCoreDatum and dasCoreUtil are unaware of each other,
and to preserve that the LoggerManager class is found in both projects.
They are functionally identical, and the one in dasCoreUtil should be
used.

# Refactoring

System.err.println -\> logger.fine

Any class that is logging should have a private or protected static
final Logger logger:

`private static final Logger logger= Logger.getLogger("qdataset.ascii");`

then this is used to log at a level of FINE or less, so scripts will not
see this message:

`logger.finest( 'found column' )`  
`logger.log( Level.FINE, "found column named {0} at {1}", new Object[]{lookFor, j} );`

If a condition is a warning that the user will want to know about, then
INFO or above can be used, but realize these messages will need to be
reported through some other mechanism as well:

`logger.log(Level.WARNING, "metadata found for key {0}, but this is not found in the ascii file parser", key);`  
`warnings.add( String.format( "metadata found for key %s, but this is not found in the ascii file parser", key ) )`

Note Netbeans likes to help out by adding code to send messages to
loggers based on the class name:

`Logger.getLogger(DataSetUtilTest.class.getName()).log(Level.SEVERE, null, ex);`

# How to turn on logging

When the application is run interactively, logging can be enabled via
the console tab, Console Settings..., and then the GUI to control log
levels. This GUI also has controls for how log messages are displayed as
well, with metadata like timing and thread identifier.

When Java is run from the command line, the Java option
"-Djava.util.logging.config.file=/tmp/mylogging.properties" is used with
the file /tmp/mylogging.properties:

`handlers=java.util.logging.ConsoleHandler`  
`java.util.logging.ConsoleHandler.level=FINEST`  
`apdss.level=FINER`  
`jython.level=FINE`

# 2020-02-02

At some point I made it so that AUTOPLOT\_DATA/config/logging.properties
is always loaded. This consistent rule works well.

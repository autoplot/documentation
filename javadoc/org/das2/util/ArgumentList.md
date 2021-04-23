# org.das2.util.ArgumentListUtility class for processing the String[] arguments passed into the main routine,
 handing positional and switch parameters.  Also automatically generates the
 usage documentation.

 Note in Autoplot's pngwalk, we add a parameter and positional argument with the
 same name.  This should continue to be supported.
ArgumentList( String programName )
creates the processor for the program.  <tt>programName</tt> is provided
 for the usage statement.  After creating the object, arguments are
 specified one by one, and then the process method is called.

***
<a name="FALSE"></a>
# FALSE



***
<a name="TRUE"></a>
# TRUE



***
<a name="addBooleanSwitchArgument"></a>
# addBooleanSwitchArgument
addBooleanSwitchArgument( String name, String abbrev, String key, String description ) &rarr; void

specify a named switch argument that is named, and we only care whether it was used or not.  e.g. --debug

### Parameters:
name - the long parameter name, which the user may enter. e.g. "level"
<br>abbrev - short (one letter) parameter version.  e.g. "l" for -l=3
<br>key - the internal reference name to get the value specified, not necessarily but often the same as name.
<br>description - a short (40 character) description of the argument.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addBooleanSwitchArgument&unscoped_q=addBooleanSwitchArgument">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addOptionalPositionArgument"></a>
# addOptionalPositionArgument
addOptionalPositionArgument( int position, String key, String defaultValue, String description ) &rarr; void

Specify the ith positional argument, which may be left unspecified by
 the user.  Note that all positional arguments after this one must also be
 optional.

### Parameters:
position - the position number, 0 is the first argument position after the class name.
<br>key - the internal reference name to get the value specified.
<br>defaultValue - the value that is returned if a value is not provided by the user.
<br>description - a short (40 character) description of the argument.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addOptionalPositionArgument&unscoped_q=addOptionalPositionArgument">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addOptionalSwitchArgument"></a>
# addOptionalSwitchArgument
addOptionalSwitchArgument( String name, String abbrev, String key, String defaultValue, String description ) &rarr; void

specify a named switch argument that may be specified by the user.  For example, --level=3 or -l=3

### Parameters:
name - the long parameter name, which the user may enter. e.g. "level"
<br>abbrev - short (one letter) parameter version.  e.g. "l" for -l=3
<br>key - the internal reference name to get the value specified, not necessarily but often the same as name.
<br>defaultValue - value to return if the user doesn't specify.  If TRUE or FALSE is used, then the
     user may use a number of different inputs such as "T" or "true", and getBooleanValue can be used to read the value
<br>description - a short (40 character) description of the argument.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addOptionalSwitchArgument&unscoped_q=addOptionalSwitchArgument">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addPositionArgument"></a>
# addPositionArgument
addPositionArgument( int position, String key, String description ) &rarr; void

Specify the ith positional argument.

### Parameters:
position - the position number, 0 is the first argument position after the class name.
<br>key - the internal reference name to get the value specified.
<br>description - a short (40 character) description of the argument.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPositionArgument&unscoped_q=addPositionArgument">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addSwitchArgument"></a>
# addSwitchArgument
addSwitchArgument( String name, String abbrev, String key, String description ) &rarr; void

specify a named switch argument that must be specified by the user.  For example, --level=3 or -l=3

### Parameters:
name - the long parameter name, which the user may enter. e.g. "level"
<br>abbrev - short (one letter) parameter version.  e.g. "l" for -l=3
<br>key - the internal reference name to get the value specified, not necessarily but often the same as name.
<br>description - a short (40 character) description of the argument.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addSwitchArgument&unscoped_q=addSwitchArgument">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBooleanValue"></a>
# getBooleanValue
getBooleanValue( String key ) &rarr; boolean



### Parameters:
key - a String

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=getBooleanValue&unscoped_q=getBooleanValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getExitCode"></a>
# getExitCode
getExitCode(  ) &rarr; int

return 0 if the exit code for a checkArgs()==false is 0 or non-zero.
 It will be 0 if --help was used.

### Returns:
the exit code.

<a href="https://github.com/autoplot/dev/search?q=getExitCode&unscoped_q=getExitCode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMap"></a>
# getMap
getMap(  ) &rarr; Map

return a Map of all the specified values.  The keys are all the internal
 String keys, and the values are all Strings.

### Returns:
a Map of the specified values, including defaults.

<a href="https://github.com/autoplot/dev/search?q=getMap&unscoped_q=getMap">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getOptions"></a>
# getOptions
getOptions(  ) &rarr; Map

returns a Map of optional arguments that were specified, so you can see
 exactly what was specified.

### Returns:
a Map of the specified values, without defaults.

<a href="https://github.com/autoplot/dev/search?q=getOptions&unscoped_q=getOptions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPreferences"></a>
# getPreferences
getPreferences(  ) &rarr; Preferences

returns the options as a java.util.prefs.Preferences object, for
 batch processes.  The idea is that a process which grabs default
 settings from the user Preferences can instead get them from the command
 line, to support batch processes.  See the Vg1pws app for an example of
 how this is used.

### Returns:
a Preferences object, loaded with the command line values.

<a href="https://github.com/autoplot/dev/search?q=getPreferences&unscoped_q=getPreferences">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getValue"></a>
# getValue
getValue( String key ) &rarr; String

get the value for this parameter

### Parameters:
key - the argument identifier.

### Returns:
the parameter's value.

<a href="https://github.com/autoplot/dev/search?q=getValue&unscoped_q=getValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="logPrefsSettings"></a>
# logPrefsSettings
logPrefsSettings( java.util.logging.Logger logger ) &rarr; void

dump the configuration to the given logger at Level.CONFIG.

### Parameters:
logger - a Logger

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=logPrefsSettings&unscoped_q=logPrefsSettings">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="makeFileReferenceAbsolute"></a>
# makeFileReferenceAbsolute
makeFileReferenceAbsolute( String ref ) &rarr; String

make a standard way to make file names absolute

### Parameters:
ref - e.g. files/afile/foo.txt

### Returns:
/home/jbf/data/files/afile/foo.txt because PWD is /home/jbf/data

<a href="https://github.com/autoplot/dev/search?q=makeFileReferenceAbsolute&unscoped_q=makeFileReferenceAbsolute">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="printPrefsSettings"></a>
# printPrefsSettings
printPrefsSettings(  ) &rarr; void

see Vg1pws app for example use.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=printPrefsSettings&unscoped_q=printPrefsSettings">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="printUsage"></a>
# printUsage
printUsage(  ) &rarr; void

print the usage statement out to stderr.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=printUsage&unscoped_q=printUsage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="process"></a>
# process
process( java.lang.String[] args ) &rarr; boolean

given the specification, process the argument list.  If the list is in error, the
 usage statement is generated, and the System.exit is called (sorry!).  Otherwise
 the method returns and getValue() may be used to retrieve the values.

 Again, note that System.exit may be called.  This is probably a bad idea and another
 method will probably be added that would return true if processing was successful.

### Parameters:
args - as in public static void main( String[] args ).

### Returns:
false if System.exit should be called.

<a href="https://github.com/autoplot/dev/search?q=process&unscoped_q=process">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="requireOneOf"></a>
# requireOneOf
requireOneOf( java.lang.String[] keyNames ) &rarr; void

requires the user specify one of these values, otherwise the usage
 statement is printed.

### Parameters:
keyNames - an array of internal key names that identify parameters.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=requireOneOf&unscoped_q=requireOneOf">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>


Purpose: Discuss the shortcomings of the Webstart launch mechanism and
identify desires and a new mechanism.

Audience: Autoplot developers, data providers and interested end-users.

# Webstart

Webstart is a mechanism provided by Oracle as a simple means of sending
applications out to end-users. A short XML file is sent to the user with
the .jnlp (x-application/jnlp mime) that is handed off to Java which
starts up with the given configuration. We've discovered it's fairly
easy to have it to send out initial configurations to end-users, but we
have also found a variety of annoyances. Some customers have been
completely unable to use it, and use the signal-jar (jumbojar) release
mechanism.

# Requirements

  - Support commonly-used Mac, Windows, and Linux platforms.
  - Provide quick initial startup (\<30 seconds on a reasonably fast
    network), and fast repeated startup (\<3 seconds).
  - Launch into initial URI or .vap file from web sites.
  - Continue to support WebStart updates.
  - Something that works 100% of the time for new Mac, Windows, and
    Linux users. This means a native installer bundled with a JRE.
  - Something that allows Mac and Windows users to use Webstart to get
    most recent version after initial install (when they used native
    installer).
  - Allow control of JVM memory. For example on 8GB machine, Autoplot
    should be allowed up to 4GB.

# See Also

  - <http://www.jwrapper.com>
  - <http://launch4j.sourceforge.net/> Ed suggested we look at this.
  - <http://www.ej-technologies.com/products/install4j/overview.html>

# Experiments with Install4j

Reza at GMU has been experimenting with Install4j.

## Notes

  - JVM size? It gets 3.5G on my Linux machine, which is great, but is
    this something we have control of?
  - The software seems a little sloppy about permissions. Like it offers
    to put links in /usr/local, but then doesn't tell me when it fails.
  - Seems to be hanging on Windows XP. This could have been because it's
    installing a new one, but it should tell me if it is slow. Worked
    fine the second time I tried. Hangs when launched from Start menu.
  - "AutoPlot" needs to be "Autoplot".
  - I was seeing where it would drop back to v2012b\_30 from v2013a\_1.
  - Needs more testing on various platforms...
  - default extensions should not include non-files, like das2server or
    cdaweb.

# Alternative Launchers

## Command line launching

  - Download the jar file
    <http://autoplot.org/jnlp/latest/autoplot.jar>. let
    $JAR="C:\\Program Files\\autoplot\\autoplot.jar"
  - Identify java location, call this $JAVA, for this example, let
    $JAVA="C:\\Program Files\\Java\\jre7\\bin\\java.exe"
  - Starting from the command line
      - $JAVA -Xms2000M -cp $JAR org.virbo.autoplot.AutoplotUI
  - The above should start without native Java support.
  - To add native support:
      - Identify the JVM bit size (32 or 64): "$JAVA -version" yeilds
        "...Java HotSpot(TM) 64-Bit Server VM ..." so this is a 64 bit
        JVM.
      - <http://autoplot.org/cdf-jnlp-3.4.1/lib/3.4.1/> contains all the
        CDF binaries, for example the Windows/64bit is
        <http://autoplot.org/cdf-jnlp-3.4.1/lib/3.4.1/windows/amd64/nativeCdfLibs.jar>
      - download the file to "C:\\Program
        Files\\autoplot\\nativeCdfLibs.jar"
      - unzip the file (jars are zip files): "$JAR xvf
        nativeCdfLibs.jar" where $JAR is the jar command found next to
        $JAVA (unzip will work as well).
      - $JAVA -Djava.library.path="C:\\Program Files\\autoplot\\"
        -Xms2000M -cp $JAR org.virbo.autoplot.AutoplotUI
  - Note in Windows a shortcut to this command ($JAVA -Xms2000M -cp $JAR
    org.virbo.autoplot.AutoplotUI) will make a useful desktop launcher.

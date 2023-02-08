
# Windows
For Windows, we have a installer.  You can go to http://autoplot.org/jnlp/latest/ and download the "exe" link.  This will run a windows installer and put in nice launchers on your machine.

# Mac
For Macs, we would normally have a .dmg that makes installation familiar, but we've had an issue where the one person who knows how to fix it is very busy with a new mission, and I haven't had time to figure out how to fix it myself.  This should be available sometime in the next six months.  So instead, you should do what the Linux people do.

# Linux, but also Mac and Windows
For Linux (or Macs or Windows), download the latest "single-jar" file, which contains the app, but does not contain Java.  You can test to see if Java is on your machine by entering at the command line:


spot9> **java -version**
<br>java version "17.0.1" 2021-10-19 LTS

(The bold is what you would type in.  "spot9" is the name of my machine, and your prompt will be different.  I happen to have Java 17 at home, but any version of Java 8 and up should work.)


Then download and save the "Single Jar" .jar file to a directory.  Supposing I save it to /home/jbf/Downloads/, I would:


spot9> **cd /home/jbf/Downloads/**    <em>(this changes to the directory, which will be different on your computer.)</em><br> 
spot9> **ls autoplot.jar**   <em>(this is going to verify that the autoplot jar is where we think it is.)</em><br>
spot9> **java -jar autoplot.jar**   <em>(this starts up Autoplot.)</em>

Things will be a little different on your computer, and if you have trouble, I would be happy to meet you by Zoom tomorrow.


Once things are going, everything should be very similar to Autoplot on other computers, but unfortunately installation is a little 
challenging.  Also newer Macs have security which must be granted to the jar file.  This can be done through the security settings after
attempting to run the application.



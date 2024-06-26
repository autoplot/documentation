Purpose: Consider upgrading to Java 6 requirement.

# Who is Affected

Just a couple of people started Autoplot with Java 5, according to the
web logs. The impact would be small.

# Reasons to Upgrade

  - KeyChain.java has writeKeysFile, which is a text file dumping all
    the known keys. With Java 6 this could be made to be readable only
    by the file's owner.
  - IOExceptions that have initial cause. Right now there is a bunch of
    code where the cause's message is preserved, but not the source
    exception.
  - Errors java 5 shows with @override annotation with inner classes.
    "./org/autoplot/pngwalk/GridPngWalkView.java:87: method does not
    override a method from its superclass" but it does...
  - java 5 shows lots of bugs with the GUIs. It works, but menus are
    drawn in the wrong place and much of the GUI takes a while to
    initially paint on Linux.

![java5gui.jpg](java5gui.jpg "java5gui.jpg")

# Notes

  - The Autoplot used by the Plasma Wave Group is already built with
    Java 6.


There are a few things that need to be done to add documentation, this
documents.

  - add javahelp folder to correct project next to source
  - add AutoplotHelp project to the dependencies for the project.
  - copy over documentation from DataSourcePack/javahelp/
  - make appropriate changes.
  - make sure Autoplot.org link has proper link, e.g.
    "<http://autoplot.org/help#ascii_main>"
  - src/META-INF/helpsets.txt
  - register the help stuff in the doc system in the java code:

AutoplotHelpSystem.getHelpSystem().registerHelpID(this, "ascii\_main");

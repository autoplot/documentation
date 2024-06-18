Purpose: record notes about using pdb in the Jython environment.
Audience: Those interested in experimenting with pdb.

# Introduction

line-by-line debugging is a dearly missed feature of IDL and Java
programming environments. These environments let you place a breakpoint
in the code, and when execution reaches the breakpoint, the application
stops and the developer can query the current state of the environment
or step through code line-by-line.

# Current State

Here's how anyone can experiment with the current state of the debugger.
Note it is easy to hang Autoplot if this is not done properly.

  - enable the debugger with:

```
 AP> from java.lang import System
 AP> System.setProperty("jythonDebugger","true")
```
  - Presently the script must be modified to use the debugger.
      - import pdb
      - pdb.set\_trace() should be called where the Jython interpreter
        should stop. An odd GUI pops up with Step and Next buttons. Also
        it shows the state of the state machine that is used to parse
        PDB output.

Note:

  - You can't debug GUI code, because the GUI thread would be hung and
    the debugger GUI would be locked up.

# See Also

  - <https://sourceforge.net/p/autoplot/feature-requests/381/>
  - <sftp://jfaden.net/home/jbf/ct/autoplot/script/demos/pythonDebugger>


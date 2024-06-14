# Audience

Scientists using Autoplot.

# Introduction

The resize dialog is raised when the canvas should be made a size which
will not fit on this machine's display. Normally, this will trigger a
dialog presenting two options. The first is to scale the .vap to a size
which would fit on to the display. Fonts are scaled, and the overall
canvas size is scaled so that it fits. The second is to use scrollbars
to access the larger canvas.

There is a system property which will avoid this dialog, resizeOption,
which can be set to "scrollbars" so that scrollbars will always be used
in this situation. This is useful when running batches where the dialog
breaks the automation. To use this, either set -DresizeOption=scrollbars
at the command line, or set it in a script like so:

```
from java.lang import System
System.setProperty('resizeOption','scrollbars')
```


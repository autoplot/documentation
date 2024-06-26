Purpose: outline syntax conversions for converting Jython code into Java
code.

Audience: Autoplot developers

# Introduction

I often have to convert a code I've prototyped in Jython to a fast
production Java code. Much of this work could be automated, and this
would be a menu item.

# Notes

|                                     |                                                               |
| ----------------------------------- | ------------------------------------------------------------- |
| from org.autoplot import AutoplotUI | import org.autoplot.AutoplotUI                                |
| inE=False                           | boolean inE= false;                                           |
| drE=None                            | Object drE= null;                                             |
| state='open'                        | String state= "open";                                         |
| while ( cond ):                     | while ( cond ) { ... }                                        |
| dsb=DataSetBuilder(2,100,2)         | DataSetBuilder dsb= new DataSetBuilder(2,100,2)               |
| tE\[iE,1\].le(tB\[iB,0\])           | datum(tE.slice(iE).slice(1)).le(datum(tB.slice(iB).slice(0))) |
| indents                             | indents turn into {}, semicolons added                        |

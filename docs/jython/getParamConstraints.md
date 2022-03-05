# Introduction
Ticket https://sourceforge.net/p/autoplot/feature-requests/360/ talks about new constraints for
the getParam calls in Jython scripts.  You've always been able to provide a list of enumerated
values for a parameter like `getParam('sc','a','spacecraft',['a','b'])` but we wish to provide
more options for constraints, and better GUI controls.  Constraints allow machines to implement
constraints, and to provide safer scripts.

When the fourth argument for the getParam call is a dictionary, it is a list of constraints.  For
example, `getParam('v',0,'volume', { 'min':0, 'max':10 } )` would be guarenteed to only return 
values from 0 to 10.  The script needn't do this safety check, and the human operator knows what
range of values are accepted.

# Implemented Constraints


| constraint | desc |  example | implementation notes |
| ---------- | ---- | -------- | --- |
| min        | minimum accepted value | 0 | some support |
| max        | maximum accepted value | 10 | some support |
| maxExclusive | maximum limit, but not allowed | 10 | proposed |
| enum | list of allowed values | ['a','b'] | supported |
| subset | values must be from this list | 'ant1,ant2,ant3' | proposed |




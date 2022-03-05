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


| constraint | example | desc | implementation notes |
| ---------- | ---- | -------- | --- |
| min        | 0 | minimum accepted value | some support |
| max        | 10 | maximum accepted value | some support |
| maxExclusive | 10 | maximum limit, but not allowed | proposed |
| enum  | ['a','b']| list of allowed values | supported, droplist shows but is not editable |
| examples | [3,5,9] | list of example values, <br>input needn't be one of these  | droplist shows but is still editable |
| subset | 'ant1,ant2,ant3' | values must be from this list |  proposed |
| regex | 'sc[1234]'  | values must match regex| some support, text GUI should warn of mismatch |
| format | '$Y-$m' | time start is formatted to this and parsed | proposed |
| format | '%.3f' | float value is formatted to this and parsed | proposed |




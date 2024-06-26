Purpose: define the format parameter for Autoplot's ascii parser.

Audience: Jeremy

# Fortran Spec

Fortran spec should be supported because many people are familiar with
it.

resource:
<http://www.tat.physik.uni-tuebingen.de/~kley/lehre/ftn77/tutorial/format.html>

number trailing is the number of characters, number preceeding is the
number of repeats: (2X, I3, 2X, I3, 2X, I3, 2X, I3) repeats of a spec:
(4(2X, I3))

```
  A - text string
  D - double precision numbers, exponent notation
  E - real numbers, exponent notation
  F - real numbers, fixed point format
  I - integer
```
further constraints: F5.3

# C sprintf spec

resource: <http://www.cplusplus.com/reference/cstdio/printf/>

printf ("floats: %4.2f %+.0e %E \\n", 3.1416, 3.1416, 3.1416);

# Python spec

resource: <http://docs.python.org/2/library/string.html#formatspec>
'%09.3f' % 56 -\> 00056.000

# Java

resource:
<http://docs.oracle.com/javase/1.5.0/docs/api/java/util/Formatter.html#syntax>

formatter.format("%2$s %s %\<s %s", "a", "b", "c", "d")


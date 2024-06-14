Purpose: Design on paper the new units handling in Autoplot.

Audience: Scientists and das2/Autoplot developers.

# Introduction

This is about the oldest unimplemented feature in Autoplot, and for that
matter das2, and data systems preceeding. Autoplot can carry around tags
for data that identify the units, but these are essentially just a
strings with a table of some conversions. Autoplot introduced new
mechanisms for declaring new Units at runtime, but these are really just
labels. The goal would be a units class such that

```
5m/10s = 0.2 m/s
```

but also

```
5 apples/10 s= 0.2 apples/s
```

and

```
2010-01-01T00:00 + 13 minutes = 2010-01-01T00:13
```

## Ratio Class

Work out some classes. It would be nice to allow 1/3 to be represented
nicely, so we introduce a Ratio class:

```
Ratio
numerator:int
denominator:int
```

Canonical form will be positive denominator.

Now to store real numbers.

```
RealNumber
scale:Ratio
exponent:Ratio
```

## Units Class

```
label:String       label for the unit, e.g. 1 * kg * m**2 * s**-3 * A**-1
scale:RealNumber   dimensionless number to scale to MKS
meters:Ratio       exponent for the meters base
kilograms:Ratio    exponent for the kilograms base
seconds:Ratio      exponent for the seconds base
ampere:Ratio       ...
kelvin:Ratio       ...
candele:Ratio      ...
mole:Ratio         ...
offsetUnits:Units  location units have an offset from some basis.  basis like "since 2014-01-01" and offset units like "microseconds"
```

# Examples

Units.pcm3 is count per cm\*\*3, as in number density.

```
Units.pcm3= Units( 'cm**-3', m=-3, scale=1e6 )
```

Units.kelvin

```
Units.kelvin= Units( 'K', K=1 )
```

Units.eV

```
Units.eV= Units( 'eV', Units.joule, scale= 1.60217653×10**19 )   # derive from previously defined units
Units.eV= Units( 'eV', kg=1, m=2, s=2, scale=1.60217653×10**19 )
```

Units.volts

```
Units.volts= Units( 'V', kg=1, m=2, s=-3, A=-1 )
```

Units.v2pm2Hz

```
Units.v2pm2Hz= Units( 'V^2 m^-2 Hz^-1', Units.volts**2, s=1, m=-2 )
```

# Parsing

CDF files and Autoplot URIs contain string representations of units we
would like to have interpretted fully. I believe with a set of rules we
could handle a good set of these strings. Also CDF has "Cluster
conventions" that enforce rules on how units are represented. For
example,these should all parse to the same unit:

`/cc&nbsp;1/cc&nbsp;cc**-1&nbsp;cc^-1&nbsp;cc!u-1!n&nbsp;cc!u-1&nbsp;cc!a-1!n&nbsp;cc`&lt;sup&gt;`-1`&lt;/sup&gt;

parenthesis are required for demoninator:

```
a/b*c   -> a * b^-1 * c
a/(b*c) -> a * b^-1 * c^-1
a b c   -> a * b * c^-1
```

```
  'V^2 m^-2 Hz^-1'
```

# Operations

  - Units\*Units -\> add all the components. Multiply the scales. If
    misc units exist, then if they are same, then ^2, else \* is used.
  - Units/Units -\> subtract the components. Divide the scales. If misc
    units exist, then 1/foo is used or foo if none. If same, foo/foo is
    ""
  - Units-Units -\> verify all components are the same. verify the
    scales are the same.
  - Units+Units -\> verify all components are the same. verify the
    scales are the same.
  - Units\*\*Units -\> not allowed unless exponent is dimensionless.

# Notes

  - Chris asked if I planned on supporting
    exa,peta,tera,giga,...,nano,femto,atto prefixes. Hadn't thought
    about that, but yes it should. He reminded me of chapter 18 from the
    PDS guide, "Units of Measurement"

<!-- end list -->

  - Unrecognized units will have to be supported. For example, we forget
    about rad (radian) but we get the unit rad/s. The system should
    register a new base "rad" and multiply it by s\*\*-1.

# Current Types of Data

Stevens has been the guiding document on the handling of Units and
Datums. He defines four types of data: nominal, ordinal, ratio, and
interval. These names are somewhat confusing, but basically:

  - **nominal** is data that simply identifies something. This can be
    "Chicago" or "Paris"; and "Science mode" or "Testing mode". The only
    operator allowed is eq (equals)
  - **ordinal** is data that has an ordering to it, like "good" "better"
    "best". eq, lt, gt, le, ge are allowed operators.
  - **interval** is data that has no meaningful zero, like
    '2017-11-03T08:36' or 32 Fahrenheit degrees. eq, lt, gt, le, ge, -,
    + of a ratio number.
  - **ratio** is data that has a meaning zero, like "13 grams". Division
    and multiplication are allowed with all other operators.

What Stevens doesn't address is things like fill data, and "modulo"
spaces, which come up often. Fill is a layer on top of other units which
identifies special values as ordinal. Typically a special value is
removed from the numbers to indicate a no-measurement condition. For
example -1e31 will indicate that a measurement could not be made. Modulo
spaces are where numbers repeat, having the same meaning each cycle. For
example, often 359 degrees and 1 degree are only 2 degrees apart.

Note das2 and Autoplot have never fully implemented this, so there are
no ordinal measurements, and modulo spaces are not implemented in the
units and datum library. TimeLocationUnits are used to represent
interval time locations and must exist between years 1000 and 9000.
TimeLocationUnits parse "NaN" as a fill value. Enumeration units
represent nominal and ordinal data, and the value "" is fill.


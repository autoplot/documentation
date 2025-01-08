Audience: Scientists and developers

# Introduction
Autoplot script input is provided through the getParam call.  This allows for constraints, for 
example a simple list of allowed values:
```
sc = getParam('sc',1,'Spacecraft Number',[1,2])
```
This only allows sc to be equal to 1 or 2.  The second and third parameters are optional.  The
constaint parameter can be a dictionary instead of an array.  Each type of parameter has different
constraints.  

Constraints are useful both at making a script more secure and also serving as 
documentation.  Most constraints will raise an exception when the constraint is not
met, others like <code>format</code> may limit resolution to desceet values.

# String parameter constraints
* <code>regex</code> the string provided must match this regex. (See Python re.match)
* <code>format</code> when the format starts with a dollar sign, the string is parsed as a time range and the minimum value is reformatted using format.

For example
```
includedModes = getParam('incl','ab', 'Include modes', { 'regex':'[abcd]+' } )
```
will allow any combination of one or more a, b, c, and d to control allowed modes, and
```
timeRange= getParam( 'timerange', '2025-01-08', 'time range', { 'format': '$Y-$m-$d' } )
```
will only allow days in the format $Y-$m-$d to be entered.

# Integer parameter constraints
* <code>min</code> the value must be greater than or equal to this value.
* <code>max</code> the value must be less than or equal to this value.

# Float parameter constraints
* <code>min</code> the value must be greater than or equal to this value.
* <code>max</code> the value must be less than or equal to this value.
* <code>format</code> when the format starts with a percent, the float is reformatted and parsed using the format.  This allows resolution to be limited.

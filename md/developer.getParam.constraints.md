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

Constraints are useful both at making a script more secure and also serving as documentation.  

# String parameter constraints

# Integer parameter constraints

# Float parameter constraints

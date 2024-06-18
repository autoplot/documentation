Purpose: revisit URI completion engine and its use cases. A number of
DataSource completion engines give colloquial responses like "<INT>". It
would be nice to tighten this up to support automatic GUI creation.

# Completion Engine

DataSource.getCompletions( CompletionContext cc ) The datasource
responds with a list of CompletionContexts. This essentially defines a
tree where:

```
  for each folder, a list of files. 
  for each file, a list of parameters
  for each parameter, a list of values (or constraint on valid values)
```
# Use Cases

  - completion engine provides efficient tool for creating URIs. (GUI
    free when you just need a little assistence)
  - URIs automatically discovered for data mining
  - Automatic GUI creation.
  - URI validation.

# Completion Engine to XML Schema

We can define a mapping from URIs to an xml document that can be
verified with an xml schema.

`&nbsp;vap+dat:`&lt;file:/path/to/file.asc?skip=45&amp;column=field5&gt;

```
 <vap+dat>
```
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;resourceUri&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;file:/path/to/file.asc&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;/resourceUri&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;params&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;skip&gt;`45`&lt;/skip&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;column&gt;`field5`&lt;/column&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;/params&gt;  
```
 </vap+dat>

 <vap+odbc>
```
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;resourceUri&gt;  
```
        mysql://192.168.0.203:3306/orbits
```
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;/resourceUri&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;params&gt;  
```
         
```
<table>

cluster1

</table>

`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;column&gt;`orbitnum`&lt;/column&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;dep0&gt;`time`&lt;/dep0&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;/params&gt;  
```
 </vap+odbc>
```
Then completion can be defined as an XML Schema.

But until then we'll use the CompletionContext object and
List<CompletionContext> getCompletions( CompletionContext ).

# API That is Useful for Automatic GUI Creation

What has to change before GUIs can be automatically created? With the
current API, we could create a GUI that is a list of parameter names
with a TextField for entering each value. Documentation strings could
provide a label for each name label and value textfield pair.

This would be unhelpful though, because users wouldn't know what is
expected in each field. We couldn't constrain fields to valid values
(e.g. <int>). It would be nice to have droplists for enumerations.
Further, sometimes a parameters are exclusive (delim and fixedColumns,
rank2 and column).

In PaPCo, we introduced a "papco\_props" idiom that tried to do this,
defining parameter groups and rules about what must be specified when.
Also, surely xml schemas provide the sophisticated rules needed to
provide a useful GUI.

But if we were to create a quick and dirty extension to what we already
have, what could be done?

  - primitive type ids like "<INT>" and "\<INT:min=0\&max=10\>"
    "\<ENUM:sc1,sc2,sc3,sc4\>" "\<SUBSET:filter1,filter2,filter3\>"
  - float primitive types might also hint at resolution to support data
    mining.
  - required keyword, perhaps with group: "required:parserType".
      - getCompletions( CompletionContext ) API supports conditional
        requirements
      - Note the data source "reject" method would no longer be
        necessary, since the completion engine can be used to see if any
        required parameters are missing.
  - some way to disable parameters so the parameter existence is
    evident, but the control is not enabled.
  - some way to hint at control type (slider vs integer text field),
    droplist vs radiobutton

## experiment

file entered: <file:/home/data/file.asc>

need type: vap+dat:/home/data/file.asc

multiple columns: column or rank2 required

## type specifiers

Examples:

```
 gzip=$(integer,min=0,max=9)
 version=$(real,format=f4.2)
 spacecraft=$(enum,values=c1,c2,c3,c4)
 filters=$(subset,values=noiseBurst,median,smooth)
 timerange=$(timerange,cadence=7d,offset=2009-001)
 $(integer,offset=4,cadence=5)  ...,-6,-1,4,9,14,...
```
TODO: name the fields so they unify with time format specification.

```
 file://foo_$(string,id=spacecraft,enum=c1,c2,c3,c4,)_$Y$m$d.dat?spacecraft=c1
```
TODO: include way to specify resource URIs like:


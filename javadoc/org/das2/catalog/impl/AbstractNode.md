# org.das2.catalog.impl.AbstractNodeAll nodes loadable by the DasNodeFactory should inherit from this package 
 private abstract class.  
 
 It supports the general 3-phase construction.  In general the construction 
 phases are:
 
 1. Create a stub object that knows what kind of thing it is and who it's 
    parents are.
 
 2. Resolve one of the URLs to get a full definition of the object.
 
 3. Possibly merge information from a secondary URL if requested.
***
<a name="getRoot"></a>
# getRoot
getRoot(  ) &rarr; DasNode



### Returns:
org.das2.catalog.DasNode


<a href="https://github.com/autoplot/dev/search?q=getRoot&unscoped_q=getRoot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRoot"></a>
# isRoot
isRoot(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isRoot&unscoped_q=isRoot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="name"></a>
# name
name(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=name&unscoped_q=name">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="path"></a>
# path
path(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=path&unscoped_q=path">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="prettyPrintLoc"></a>
# prettyPrintLoc
prettyPrintLoc( String sPre, String sSep ) &rarr; String

Get the root node list as a string with some separator and prefix

### Parameters:
sPre - A prefix to place before each root node URL, may be null
<br>sSep - The separator to use between each root node URL, may be null

### Returns:
A formatted string containing a list of all root node URLs

<a href="https://github.com/autoplot/dev/search?q=prettyPrintLoc&unscoped_q=prettyPrintLoc">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>


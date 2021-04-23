# org.das2.catalog.DasPropProperties retrieved from a das catalog node, a wrapper around Object.  

 DasNodes can have properties of different types.  Since Java reflection provides
 methods for determining the actual return type of a property pulled from a catalog
 node, introducing a property type seems on it's face to be an unnecessary 
 complication.  However to avoid having a completely open ended interface that can
 return just any type of object this class exists to put boundaries around the
 value types an application program will have to deal with when reading from a das
 catalog.  
 
 Without this class, constructs like the following would be common in application
 code:
 
    String sFragment = "interface/data/efield/units";
    Object obj = node.prop(sFragment, Map<String,Object>.class);
    Map<String,Object> map = (Map<String,Object>)obj;
 
 Instead this becomes:
   
    Map<String,DasProp> map = node.prop("interface/data/efield/units").map();
DasProp( Object item )
Wrap a raw object and give it a type.
 
 This constructor does not handle parsing of string objects to some
 other type.  To parse strings use the two-parameter constructor.

***
<a name="NULL"></a>
# NULL



***
<a name="BOOL"></a>
# BOOL



***
<a name="STR"></a>
# STR



***
<a name="INT"></a>
# INT



***
<a name="DATUM"></a>
# DATUM



***
<a name="TIME"></a>
# TIME



***
<a name="LIST"></a>
# LIST



***
<a name="MAP"></a>
# MAP



***
<a name="list"></a>
# list
list(  ) &rarr; List



### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=list&unscoped_q=list">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="map"></a>
# map
map(  ) &rarr; Map



### Returns:
java.util.Map


<a href="https://github.com/autoplot/dev/search?q=map&unscoped_q=map">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

map( String sKey ) &rarr; DasProp<br>
***
<a name="str"></a>
# str
str(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=str&unscoped_q=str">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="time"></a>
# time
time(  ) &rarr; ZonedDateTime



### Returns:
java.time.ZonedDateTime


<a href="https://github.com/autoplot/dev/search?q=time&unscoped_q=time">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>


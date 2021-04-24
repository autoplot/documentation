# org.das2.datum.Orbits

Orbits are a map of string identifiers to DatumRanges, typically used to enumerate the orbits a spacecraft makes.
 For example, Cassini orbit "C" was from 2004-366T07:03 to 2005-032T03:27 and "33" was from  2006-318T23:34 to 2006-330T22:23.
 There are two types of orbits: canonical, which have an identifier like "cassini" and can be used by the community, and user
 which have identifiers like  http://das2.org/wiki/index.php/testorbits .  In either case, these refer to a file.
 The canonical ones are stored on the das2 wiki at  http://das2.org/wiki/index.php/Orbits/&lt;id&gt;.  This file is a
 three-column ascii file with the orbit id in either the first or last column.  Note any line not meeting this spec is ignored,
 so that orbit files can contain additional documentation (and can sit within a wiki).

***
<a name="compare"></a>
# compare
compare( String a, String b ) &rarr; int

return -1 if a is before b, 0 if they are equal, and 1 if a is after b.

### Parameters:
a - a String
<br>b - a String

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=compare&unscoped_q=compare">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="first"></a>
# first
first(  ) &rarr; String

return the first orbit id, so that we can iterate through all

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=first&unscoped_q=first">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDatumRange"></a>
# getDatumRange
getDatumRange( String orbit ) &rarr; DatumRange

return the DatumRange for this orbit number.  Note this IS NOT an OrbitDatumRange.

### Parameters:
orbit - a String

### Returns:
a DatumRange


<a href="https://github.com/autoplot/dev/search?q=getDatumRange&unscoped_q=getDatumRange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getOrbit"></a>
# getOrbit
getOrbit( Datum d ) &rarr; String

returns the first orbit containing the time, or null if none do.

### Parameters:
d - a Datum

### Returns:
the orbit number or null

<a href="https://github.com/autoplot/dev/search?q=getOrbit&unscoped_q=getOrbit">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getOrbitOnOrBefore"></a>
# getOrbitOnOrBefore
getOrbitOnOrBefore( Datum d ) &rarr; String

return the closest orbit on or before datum d.

### Parameters:
d - the datum

### Returns:
the id of the closest orbit before, or null.
### See Also:
<a href='http://jfaden.net/~jbf/autoplot/script/demos/jeremy/onOrBefore.jy'>http://jfaden.net/~jbf/autoplot/script/demos/jeremy/onOrBefore.jy</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getOrbitOnOrBefore&unscoped_q=getOrbitOnOrBefore">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getOrbitsFor"></a>
# getOrbitsFor
getOrbitsFor( String sc ) &rarr; Orbits

Return the orbits for the named spacecraft, or those described in the file pointed to the URL when
 the "sc" identifier is a URL.

 Example files may be on the wiki page http://das2.org/wiki/index.php/Orbits.&lt;SC%gt;,
 or on the classpath in /orbits/&lt;SC&gt;.dat  The orbits file will be read by ignoring any line
 that does not contain three non-space blobs, and either the first two or last two should parse as an
 ISO8601 string.  The ISO8601 strings must start with 4-digit years, either
 Note the input can then be html, with a pre section containing the orbits.

 Note the wiki page is the source for cassini and crres, but other missions may come from special places encoded here.
 Mediawiki introduced two problems: first, that typos were not identified clearly because a 200 (ok) code is returned
 for any URL.  Second, it's not trivial to set up mirrors that put data into the wiki.  For this reason, the wiki
 should only be used as a reference for humans and other use is discouraged.

 This now uses special code for rbspb-pp and rbspa-pp that looks at UIowa, LANL and at virbo.org.

 This should not be called from the event thread, because it may block briefly while the orbits are loaded.

### Parameters:
sc - the string identifier for the spacecraft, such as "rbspa-pp", or URL to orbit file.

### Returns:
the Orbits file which can be used to query orbits.

<a href="https://github.com/autoplot/dev/search?q=getOrbitsFor&unscoped_q=getOrbitsFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSpacecraft"></a>
# getSpacecraft
getSpacecraft(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getSpacecraft&unscoped_q=getSpacecraft">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSpacecraftIdExamples"></a>
# getSpacecraftIdExamples
getSpacecraftIdExamples(  ) &rarr; Map

return examples of spacecraft ids which can be used, and a human-readable label
 in a linked hash map.  This may fall out-of-sync with the list of IDs which
 would work (see https://das2.org/Orbits/), but this should be considered a bug.

### Returns:
map from id to description.

<a href="https://github.com/autoplot/dev/search?q=getSpacecraftIdExamples&unscoped_q=getSpacecraftIdExamples">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getURL"></a>
# getURL
getURL(  ) &rarr; URL

return the URL used to populate the orbits.

### Returns:
a java.net.URL


<a href="https://github.com/autoplot/dev/search?q=getURL&unscoped_q=getURL">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isOrbitsFile"></a>
# isOrbitsFile
isOrbitsFile( String sc ) &rarr; boolean

provide method for clients to see if the URI represents an orbits file, without 
 constantly going into the synchronized block, which was causing things to hang for
 Masafumi.

### Parameters:
sc - the string identifier for the spacecraft, such as "rbspa-pp", or URL to orbit file.

### Returns:
true if the uri refers to orbits.

<a href="https://github.com/autoplot/dev/search?q=isOrbitsFile&unscoped_q=isOrbitsFile">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="last"></a>
# last
last(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=last&unscoped_q=last">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="next"></a>
# next
next( String orbit ) &rarr; String

return the next orbit number, or null if there are no more orbit numbers.

### Parameters:
orbit - a String

### Returns:
the orbit number or null.

<a href="https://github.com/autoplot/dev/search?q=next&unscoped_q=next">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="prev"></a>
# prev
prev( String orbit ) &rarr; String

return the previous orbit number, or null if there are no more orbit numbers.

### Parameters:
orbit - a String

### Returns:
the orbit number or null.

<a href="https://github.com/autoplot/dev/search?q=prev&unscoped_q=prev">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reset"></a>
# reset
reset(  ) &rarr; void

reset the loaded missions.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reset&unscoped_q=reset">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="trimOrbit"></a>
# trimOrbit
trimOrbit( String orbit ) &rarr; String

Orbit numbers are typically just a number, but some missions like Cassini had letter names for orbits
 as well.  This encapsulates the code to identify the canonical orbit from the string, by
 removing trailing _'s and 0's.

### Parameters:
orbit - a String

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=trimOrbit&unscoped_q=trimOrbit">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>


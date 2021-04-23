# org.das2.util.AboutUtil

method for getting useful build and version information.
 TODO: Splash should call this to get version, not the other way around.

# AboutUtil( )


***
<a name="getAboutHtml"></a>
# getAboutHtml
getAboutHtml(  ) &rarr; String

return HTML code describing the release version, Java version, build time, etc.

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getAboutHtml&unscoped_q=getAboutHtml">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBuildInfos"></a>
# getBuildInfos
getBuildInfos(  ) &rarr; List

searches class path for META-INF/build.txt, returns nice strings

### Returns:
one line per jar

<a href="https://github.com/autoplot/dev/search?q=getBuildInfos&unscoped_q=getBuildInfos">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getJenkinsURL"></a>
# getJenkinsURL
getJenkinsURL(  ) &rarr; String

Identify the release by looking for build.jenkinsURL .  It's expected
 that the build script will insert build.tag into META-INF/build.txt

### Returns:
build URL, or "" if one is not found.

<a href="https://github.com/autoplot/dev/search?q=getJenkinsURL&unscoped_q=getJenkinsURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getReleaseTag"></a>
# getReleaseTag
getReleaseTag( java.lang.Class clas ) &rarr; String

return the tag assigned to the class, but looking for "META-INF/build.txt" in the jar file.

### Parameters:
clas - a java.lang.Class

### Returns:
release tag or "(dev)" if the tag is not found.

<a href="https://github.com/autoplot/dev/search?q=getReleaseTag&unscoped_q=getReleaseTag">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getReleaseTag(  ) &rarr; String<br>
***
<a name="isJreVersionAtLeast"></a>
# isJreVersionAtLeast
isJreVersionAtLeast( String neededVersion ) &rarr; boolean

evaluate if the current JRE version is at least a given level.  This
 was introduced that

### Parameters:
neededVersion - the Java version, such as "1.8.0_102"

### Returns:
true if the JRE is at least the version, or if the JRE cannot be parsed.

<a href="https://github.com/autoplot/dev/search?q=isJreVersionAtLeast&unscoped_q=isJreVersionAtLeast">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>


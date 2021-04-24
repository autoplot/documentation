# org.das2.util.filesystem.Glob

known bug: *.java matches ".java". The unix glob behavior is to
 require that a leading . must be explicitly matched.

# Glob( )


***
<a name="getGlobFileFilter"></a>
# getGlobFileFilter
getGlobFileFilter( String glob ) &rarr; FileFilter



### Parameters:
glob - a String

### Returns:
javax.swing.filechooser.FileFilter


<a href="https://github.com/autoplot/dev/search?q=getGlobFileFilter&unscoped_q=getGlobFileFilter">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getGlobFromRegex"></a>
# getGlobFromRegex
getGlobFromRegex( String regex ) &rarr; String

converts regex into a glob, as best it can.

### Parameters:
regex - regular expression like "foo.\*\.dat"

### Returns:
a glob like "foo*.dat"

<a href="https://github.com/autoplot/dev/search?q=getGlobFromRegex&unscoped_q=getGlobFromRegex">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPattern"></a>
# getPattern
getPattern( String glob ) &rarr; Pattern

converts a glob into a Pattern.

### Parameters:
glob - a string like '*.dat'

### Returns:
a Pattern for the glob, for example *.dat -> .*\.dat

<a href="https://github.com/autoplot/dev/search?q=getPattern&unscoped_q=getPattern">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRegex"></a>
# getRegex
getRegex( String glob ) &rarr; String

converts a glob into a regex.

### Parameters:
glob - a String

### Returns:
the regular expression that implements, like 'foo.*\.dat'

<a href="https://github.com/autoplot/dev/search?q=getRegex&unscoped_q=getRegex">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="unGlob"></a>
# unGlob
unGlob( org.das2.util.filesystem.FileSystem fs, String glob ) &rarr; FileObject

unglob the glob into an array of the matching FileObjects.
 See sftp://papco.org/home/jbf/ct/autoplot/script/demos/filesystem/unGlobDemo.jy

### Parameters:
fs - the filesystem
<br>glob - the glob, such as '/*.gif'

### Returns:
an array of FileObjects that match the glob.

<a href="https://github.com/autoplot/dev/search?q=unGlob&unscoped_q=unGlob">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>


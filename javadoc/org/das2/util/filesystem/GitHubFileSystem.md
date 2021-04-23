# org.das2.util.filesystem.GitHubFileSystemGitHubFileSystem allows GitHub directories to be mounted directly, even 
 though it is not a conventional filesystem with files residing in folders.  
 For example, the file resource README.md found in 
 https://github.com/autoplot/scripts/ is downloaded from 
 https://github.com/autoplot/scripts/blob/master/README.md,
 with "blob/master/" added to the URL.  Likewise directory "demos" is found
 under "tree/master/".
 
 GitHub also introduced a new problem, where dates cannot be used for 
 evaluating file freshness.  ETags are now supported in WebFileSystem to 
 provide this functionality.
 
 Note, there's a strange interaction with Java and GitHub.com, where Java's
 caching prevents updates from appearing automatically.  See
 https://sourceforge.net/p/autoplot/bugs/2203/ .
***
<a name="createGitHubFileSystem"></a>
# createGitHubFileSystem
createGitHubFileSystem( java.net.URI root ) &rarr; GitHubFileSystem

create GitLabs instance

### Parameters:
root - the root

### Returns:
the filesystem.

<a href="https://github.com/autoplot/dev/search?q=createGitHubFileSystem&unscoped_q=createGitHubFileSystem">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

createGitHubFileSystem( java.net.URI root, int baseOffset ) &rarr; GitHubFileSystem<br>
***
<a name="getLocalRoot"></a>
# getLocalRoot
getLocalRoot( java.net.URI root ) &rarr; File

return the location within the file cache of this GitHub filesystem.
 TODO: There's something with branches that still needs work.  Also the constructor
 does not use this.

### Parameters:
root - an URI

### Returns:
the directory containing the resource.

<a href="https://github.com/autoplot/dev/search?q=getLocalRoot&unscoped_q=getLocalRoot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getURI"></a>
# getURI
getURI( String filename ) &rarr; URI



### Parameters:
filename - a String

### Returns:
java.net.URI


<a href="https://github.com/autoplot/dev/search?q=getURI&unscoped_q=getURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getURL"></a>
# getURL
getURL( String filename ) &rarr; URL

return the URL for the internal filename

### Parameters:
filename - internal filename

### Returns:
a java.net.URL


<a href="https://github.com/autoplot/dev/search?q=getURL&unscoped_q=getURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="gitHubMapDir"></a>
# gitHubMapDir
gitHubMapDir( java.net.URI root, String filename ) &rarr; URL

github puts directories for each project under "tree/master".

### Parameters:
root - an URI
<br>filename - a String

### Returns:
a java.net.URL


<a href="https://github.com/autoplot/dev/search?q=gitHubMapDir&unscoped_q=gitHubMapDir">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="gitHubMapFile"></a>
# gitHubMapFile
gitHubMapFile( java.net.URI root, String filename ) &rarr; URL

Given the URI, convert this to the link which will download the file.
 github puts directories for each project under "raw/master".

### Parameters:
root - an URI
<br>filename - a String

### Returns:
Translate:<pre>%{code
 https://abbith.physics.uiowa.edu/jbf/myawesomepublicproject/blob/24dff04b9bcb275d8bfd85b38e0e8b039b21d655/sayAwesome.jy to <br>
 https://abbith.physics.uiowa.edu/jbf/myawesomepublicproject/raw/24dff04b9bcb275d8bfd85b38e0e8b039b21d655/sayAwesome.jy
 https://github.com/autoplot/app/raw/master/Autoplot/src/resources/badge_ok.png to
 https://github.com/autoplot/app/master/Autoplot/src/resources/badge_ok.png
 https://jfaden.net/git/jbfaden/public/blob/master/u/jeremy/2019/20191023/updates.jy

 https://research-git.uiowa.edu/space-physics/juno/ap-script/master/test/testap.jy to
 https://research-git.uiowa.edu/space-physics/juno/ap-script/-/raw/master/test/testap.jy 

 https://research-git.uiowa.edu/jbf/testproject/-/blob/master/script/testScript.jy to
 https://research-git.uiowa.edu/jbf/testproject/master/script/testScript.jy
 }
 </pre>

<a href="https://github.com/autoplot/dev/search?q=gitHubMapFile&unscoped_q=gitHubMapFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isGithubFileSystem"></a>
# isGithubFileSystem
isGithubFileSystem( String h, String path ) &rarr; String

one place that lists the GitHub (GitLab) filesystems.

### Parameters:
h - the host
<br>path - path to the top of the GitLabs instance.

### Returns:
null if it is not a GitHub filesystem, or the initial path otherwise

<a href="https://github.com/autoplot/dev/search?q=isGithubFileSystem&unscoped_q=isGithubFileSystem">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="listDirectory"></a>
# listDirectory
listDirectory( String directory ) &rarr; String



### Parameters:
directory - a String

### Returns:
java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=listDirectory&unscoped_q=listDirectory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="strjoin"></a>
# strjoin
strjoin( java.lang.String[] c, String delim, int start, int end ) &rarr; String

this will be replaced in Java 8.

### Parameters:
c - a java.lang.String[]
<br>delim - a String
<br>start - positive index, or negative from end.
<br>end - positive index, or negative from end.

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=strjoin&unscoped_q=strjoin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>


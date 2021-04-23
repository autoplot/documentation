# org.autoplot.datasource.HtmlResponseIOExceptionAllow special exception to be thrown when Html source code is returned when
 something else was expected.  This might happen when:
  1. a file reference on autoplot.org is not found, and mediawiki returns an human-readable error page instead of a 404 page.
  2. a hotel or coffee house login screen is returned until the user logs in.
 We can look for this exception type, and present the page instead of a confusing error.
HtmlResponseIOException( String s, java.net.URL url )


***
<a name="getURL"></a>
# getURL
getURL(  ) &rarr; URL



### Returns:
java.net.URL


<a href="https://github.com/autoplot/dev/search?q=getURL&unscoped_q=getURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>


# org.autoplot.servletutil.InsertDas2UserIntoVapAt the RPW Group, we need to rewrite the vap so that the username is known to the Das2ServerDataSource.
InsertDas2UserIntoVap( )


***
<a name="insertExtraParams"></a>
# insertExtraParams
insertExtraParams( java.io.File vap, java.io.File o, String vapScheme, java.util.Map extraParams ) &rarr; void

insert extra parameters into the URIs, where the vapScheme is found.

### Parameters:
vap - the original vap
<br>o - the new vap, which will be written
<br>vapScheme - the URI type to match.  E.g. "vap+das2server"
<br>extraParams - the parameters to insert into the matching URIs.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=insertExtraParams&unscoped_q=insertExtraParams">[search for examples]</a>


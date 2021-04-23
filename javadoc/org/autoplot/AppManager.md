# org.autoplot.AppManagerCount the number of open applications and call exit when there are zero.
AppManager( )


***
<a name="addApplication"></a>
# addApplication
addApplication( Object app ) &rarr; void



### Parameters:
app - an Object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addApplication&unscoped_q=addApplication">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addCloseCallback"></a>
# addCloseCallback
addCloseCallback( Object app, String id, org.autoplot.AppManager.CloseCallback c ) &rarr; void

add a close callback which can prevent a close.  The callback
 can open a dialog requesting that the user save a file, for example.

### Parameters:
app - to associate the callback.
<br>id - a String
<br>c - an AppManager.CloseCallback

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addCloseCallback&unscoped_q=addCloseCallback">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="closeApplication"></a>
# closeApplication
closeApplication( Object app ) &rarr; void



### Parameters:
app - an Object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=closeApplication&unscoped_q=closeApplication">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getApplication"></a>
# getApplication
getApplication( int i ) &rarr; Object



### Parameters:
i - an int

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getApplication&unscoped_q=getApplication">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getApplicationCount"></a>
# getApplicationCount
getApplicationCount(  ) &rarr; int

return the number of running applications this AppManager is managing.

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=getApplicationCount&unscoped_q=getApplicationCount">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInstance"></a>
# getInstance
getInstance(  ) &rarr; AppManager



### Returns:
org.autoplot.AppManager


<a href="https://github.com/autoplot/dev/search?q=getInstance&unscoped_q=getInstance">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getWindowListener"></a>
# getWindowListener
getWindowListener( Object app, javax.swing.Action closeAction ) &rarr; WindowListener



### Parameters:
app - an Object
<br>closeAction - an Action

### Returns:
java.awt.event.WindowListener


<a href="https://github.com/autoplot/dev/search?q=getWindowListener&unscoped_q=getWindowListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getWindowListener( Object app ) &rarr; WindowListener<br>
***
<a name="isRunningApplication"></a>
# isRunningApplication
isRunningApplication( Object app ) &rarr; boolean

return true if the application is registered.  This was introduced
 so that ScriptContext could check that it hasn't been closed.  (This 
 listens to window closing events.)

### Parameters:
app - an Object

### Returns:
true if the app is still registered.

<a href="https://github.com/autoplot/dev/search?q=isRunningApplication&unscoped_q=isRunningApplication">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="quit"></a>
# quit
quit(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=quit&unscoped_q=quit">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

quit( int status ) &rarr; void<br>
***
<a name="requestClose"></a>
# requestClose
requestClose( Object app ) &rarr; boolean

returns true if close can be called, exiting the program.  If the callback throws an exception, then a warning is displayed.  I expect
 this will often occur in scripts.

### Parameters:
app - the app that is closing.

### Returns:
true if the callback okays the close.

<a href="https://github.com/autoplot/dev/search?q=requestClose&unscoped_q=requestClose">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="requestQuit"></a>
# requestQuit
requestQuit(  ) &rarr; boolean

returns true if quit can be called, exiting the program.  If the callback throws an exception, then a warning is displayed.  I expect
 this will often occur in scripts.

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=requestQuit&unscoped_q=requestQuit">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>


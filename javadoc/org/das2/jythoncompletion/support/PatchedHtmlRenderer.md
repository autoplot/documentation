# org.das2.jythoncompletion.support.PatchedHtmlRenderer

Temporary patched {@link org.openide.awt.HtmlRenderer} to allow disabling
 of the color change in case when the particular item is selected.

***
<a name="STYLE_CLIP"></a>
# STYLE_CLIP

Constant used by {@link #renderString renderString}, {@link #renderPlainString renderPlainString},
 {@link #renderHTML renderHTML}, and {@link Renderer#setRenderStyle}
 if painting should simply be cut off at the boundary of the cooordinates passed.

***
<a name="STYLE_TRUNCATE"></a>
# STYLE_TRUNCATE

Constant used by {@link #renderString renderString}, {@link #renderPlainString renderPlainString},
 {@link #renderHTML renderHTML}, and {@link Renderer#setRenderStyle} if
 painting should produce an ellipsis (...)
 if the text would overlap the boundary of the coordinates passed.

***
<a name="renderHTML"></a>
# renderHTML
renderHTML( String s, java.awt.Graphics g, int x, int y, int w, int h, java.awt.Font f, java.awt.Color defaultColor, int style, boolean paint, boolean disableColorChange ) &rarr; double

Render a string as HTML using a fast, lightweight renderer supporting a limited
 subset of HTML.  See class Javadoc for details.

 <P>
 This method can also be used in non-painting mode to establish the space
 necessary to paint a string.  This is accomplished by passing the value of the
 <code>paint</code> argument as false.  The return value will be the required
 width in pixels
 to display the text.  Note that in order to retrieve an
 accurate value, the argument for available width should be passed
 as {@link Integer#MAX_VALUE} or an appropriate maximum size - otherwise
 the return value will either be the passed maximum width or the required
 width, whichever is smaller.  Also, the clip shape for the passed graphics
 object should be null or a value larger than the maximum possible render size.
 <P>
 This method will log a warning if it encounters HTML markup it cannot
 render.  To aid diagnostics, if NetBeans is run with the argument
 <code>-J-Dnetbeans.lwhtml.strict=true</code> an exception will be thrown
 when an attempt is made to render unsupported HTML.

### Parameters:
s - The string to render
<br>g - A graphics object into which the string should be drawn, or which should be
 used for calculating the appropriate size
<br>x - The x coordinate to paint at.
<br>y - The y position at which to paint.  Note that this method does not calculate font
 height/descent - this value should be the baseline for the line of text, not
 the upper corner of the rectangle to paint in.
<br>w - The maximum width within which to paint.
<br>h - The maximum height within which to paint.
<br>f - The base font to be used for painting or calculating string width/height.
<br>defaultColor - The base color to use if no font color is specified as html tags
<br>style - The wrapping style to use, either {@link #STYLE_CLIP},
 or {@link #STYLE_TRUNCATE}
<br>paint - True if actual painting should occur.  If false, this method will not actually
 paint anything, only return a value representing the width/height needed to
 paint the passed string.
<br>disableColorChange - a boolean

### Returns:
The width in pixels required
 to paint the complete string, or the passed parameter <code>w</code> if it is
 smaller than the required width.

<a href="https://github.com/autoplot/dev/search?q=renderHTML&unscoped_q=renderHTML">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="renderPlainString"></a>
# renderPlainString
renderPlainString( String s, java.awt.Graphics g, int x, int y, int w, int h, java.awt.Font f, java.awt.Color defaultColor, int style, boolean paint ) &rarr; double

Render a string to a graphics instance, using the same API as {@link #renderHTML renderHTML}.
 Can render a string using JLabel-style ellipsis (...) in the case that
 it will not fit in the passed rectangle, if the style parameter is
 {@link #STYLE_CLIP}. Returns the width in pixels successfully painted.
 <strong>This method is not thread-safe and should not be called off
 the AWT thread.</strong>

### Parameters:
s - a String
<br>g - a Graphics
<br>x - an int
<br>y - an int
<br>w - an int
<br>h - an int
<br>f - a Font
<br>defaultColor - a Color
<br>style - an int
<br>paint - a boolean

### Returns:
double

### See Also:
<a href='#renderHTML'>renderHTML</a> <br>

<a href="https://github.com/autoplot/dev/search?q=renderPlainString&unscoped_q=renderPlainString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="renderString"></a>
# renderString
renderString( String s, java.awt.Graphics g, int x, int y, int w, int h, java.awt.Font f, java.awt.Color defaultColor, int style, boolean paint ) &rarr; double

Render a string to a graphics context, using HTML markup if the string
 begins with <code>&lt;html&gt;</code>.  Delegates to {@link #renderPlainString renderPlainString}
 or {@link #renderHTML renderHTML} as appropriate.  See the class documentation for
 for details of the subset of HTML that is
 supported.

### Parameters:
s - The string to render
<br>g - A graphics object into which the string should be drawn, or which should be
 used for calculating the appropriate size
<br>x - The x coordinate to paint at.
<br>y - The y position at which to paint.  Note that this method does not calculate font
 height/descent - this value should be the baseline for the line of text, not
 the upper corner of the rectangle to paint in.
<br>w - The maximum width within which to paint.
<br>h - The maximum height within which to paint.
<br>f - The base font to be used for painting or calculating string width/height.
<br>defaultColor - The base color to use if no font color is specified as html tags
<br>style - The wrapping style to use, either {@link #STYLE_CLIP},
 or {@link #STYLE_TRUNCATE}
<br>paint - True if actual painting should occur.  If false, this method will not actually
 paint anything, only return a value representing the width/height needed to
 paint the passed string.

### Returns:
The width in pixels required
 to paint the complete string, or the passed parameter <code>w</code> if it is
 smaller than the required width.

<a href="https://github.com/autoplot/dev/search?q=renderString&unscoped_q=renderString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>


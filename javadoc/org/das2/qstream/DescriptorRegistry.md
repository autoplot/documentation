# org.das2.qstream.DescriptorRegistry

Registry for XML elements that appear on QStreams.  The tag name is used
 to register the element.

# DescriptorRegistry( )


***
<a name="get"></a>
# get
get( String s ) &rarr; DescriptorFactory

look up the factory used for the tag name

### Parameters:
s - the tag name

### Returns:
the factory

<a href="https://github.com/autoplot/dev/search?q=get&unscoped_q=get">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="register"></a>
# register
register( String s, org.das2.qstream.DescriptorFactory factory ) &rarr; void

register the factory used for the tag name.

### Parameters:
s - the tag name
<br>factory - the factory

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=register&unscoped_q=register">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>


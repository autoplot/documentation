# org.das2.qstream.SerialStreamFormatter

We need a class that can format a stream serially.  SimpleStreamFormatter needs the whole dataset, which really
 misses the point with QStreams, that you can process and create data streams serially on the server side.  The
 das2stream codes were first coded with this use case, but QStreams were not and because of this a good serial
 generator was never created.

 See the main method for an example of how this is used.

 Note this class is not thread-safe and assumes that only one thread will be working on the stream.  This may change.

# SerialStreamFormatter( )


***
<a name="DEFAULT_TIME_DIGITS"></a>
# DEFAULT_TIME_DIGITS



***
<a name="INOUTFORM_INLINE"></a>
# INOUTFORM_INLINE



***
<a name="INOUTFORM_ONE_RECORD"></a>
# INOUTFORM_ONE_RECORD



***
<a name="INOUTFORM_STREAMING"></a>
# INOUTFORM_STREAMING



***
<a name="format"></a>
# format
format( String joinName, String name, QDataSet ds1, String inoutForm ) &rarr; void

format the dataset, maybe sending a descriptor if it hasn't been sent already.

### Parameters:
joinName - the name to which we join the dataset.
<br>name - the name for the dataset of which ds1 is all or a slice of, or null.
<br>ds1 - a QDataSet
<br>inoutForm - one of "inline", "oneRecord", or "streaming"

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=format&unscoped_q=format">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

format( String name, QDataSet ds1, String inoutForm ) &rarr; void<br>
***
<a name="init"></a>
# init
init( String name, java.nio.channels.WritableByteChannel out ) &rarr; void

the name of the default dataset.

### Parameters:
name - a String
<br>out - a WritableByteChannel

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=init&unscoped_q=init">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

init( String name, org.das2.qstream.StreamHandler sh ) &rarr; void<br>
***
<a name="isAsciiTypes"></a>
# isAsciiTypes
isAsciiTypes(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isAsciiTypes&unscoped_q=isAsciiTypes">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isBigEndian"></a>
# isBigEndian
isBigEndian(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isBigEndian&unscoped_q=isBigEndian">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="join"></a>
# join
join( String name, int rank, java.util.Map props ) &rarr; void



### Parameters:
name - a String
<br>rank - an int
<br>props - a java.util.Map

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=join&unscoped_q=join">[search for examples]</a>
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
<a name="maybeFormat"></a>
# maybeFormat
maybeFormat( String name, QDataSet ds1, String inoutForm ) &rarr; void

format the dataset, maybe sending a descriptor if it hasn't been sent already.
 ds1 may be null in this function, in which case nothing needs to be done.

### Parameters:
name - the name for the dataset of which ds1 is all or a slice of, or null.
<br>ds1 - a QDataSet
<br>inoutForm - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=maybeFormat&unscoped_q=maybeFormat">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="retire"></a>
# retire
retire( String name ) &rarr; void

allow the stream to recycle the name.  new packets with this name will issue a new packetDescriptor.

### Parameters:
name - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=retire&unscoped_q=retire">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAsciiTypes"></a>
# setAsciiTypes
setAsciiTypes( boolean asciiTypes ) &rarr; void



### Parameters:
asciiTypes - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAsciiTypes&unscoped_q=setAsciiTypes">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setBigEndian"></a>
# setBigEndian
setBigEndian( boolean bigEndian ) &rarr; void



### Parameters:
bigEndian - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setBigEndian&unscoped_q=setBigEndian">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTransferType"></a>
# setTransferType
setTransferType( String name, org.das2.qstream.TransferType tt ) &rarr; void

explicitly set the transfer type.

### Parameters:
name - a String
<br>tt - a TransferType

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTransferType&unscoped_q=setTransferType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setUnitTransferType"></a>
# setUnitTransferType
setUnitTransferType( Units u, org.das2.qstream.TransferType tt ) &rarr; void

explicitly set the transfer type used to transfer data that is convertible to this
 unit.

### Parameters:
u - an Units
<br>tt - a TransferType

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUnitTransferType&unscoped_q=setUnitTransferType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>


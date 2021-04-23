# org.das2.stream.MicrophoneStream



# MicrophoneStream( javax.sound.sampled.TargetDataLine line, javax.sound.sampled.AudioFileFormat.Type targetType, java.io.File file )


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
<a name="run"></a>
# run
run(  ) &rarr; void

Main working method.
	    You may be surprised that here, just 'AudioSystem.write()' is
	    called. But internally, it works like this: AudioSystem.write()
	    contains a loop that is trying to read from the passed
	    AudioInputStream. Since we have a special AudioInputStream
	    that gets its data from a TargetDataLine, reading from the
	    AudioInputStream leads to reading from the TargetDataLine. The
	    data read this way is then written to the passed File. Before
	    writing of audio data starts, a header is written according
	    to the desired audio file type. Reading continues untill no
	    more data can be read from the AudioInputStream. In our case,
	    this happens if no more data can be read from the TargetDataLine.
	    This, in turn, happens if the TargetDataLine is stopped or closed
	    (which implies stopping). (Also see the comment above.) Then,
	    the file is closed and 'AudioSystem.write()' returns.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=run&unscoped_q=run">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="start"></a>
# start
start(  ) &rarr; void

Starts the recording.
	    To accomplish this, (i) the line is started and (ii) the
	    thread is started.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=start&unscoped_q=start">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="stopRecording"></a>
# stopRecording
stopRecording(  ) &rarr; void

Stops the recording.

	    Note that stopping the thread explicitely is not necessary. Once
	    no more data can be read from the TargetDataLine, no more data
	    be read from our AudioInputStream. And if there is no more
	    data from the AudioInputStream, the method 'AudioSystem.write()'
	    (called in 'run()' returns. Returning from 'AudioSystem.write()'
	    is followed by returning from 'run()', and thus, the thread
	    is terminated automatically.

	    It's not a good idea to call this method just 'stop()'
	    because stop() is a (deprecated) method of the class 'Thread'.
	    And we don't want to override this method.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=stopRecording&unscoped_q=stopRecording">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>


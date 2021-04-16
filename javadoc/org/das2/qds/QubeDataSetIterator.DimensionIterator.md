# org.das2.qds.QubeDataSetIterator.DimensionIteratorDimensionIterator iterates over an index.  For example, using 
 Jython for brevity:
<blockquote><pre><small>{@code
 ds= zeros(15,4,2)
 ds[:,:,:] has itertors that count of 0,...,14; 0,...,3; and 0,1
 ds[3:15,:,:]  uses a StartStopStepIterator to count off 3,4,5,...,14
 ds[3,:,:]  uses a SingletonIterator
 i1= [0,1,2,3]
 i2= [0,0,1,1]
 i3= [0,1,0,1]
 ds[i1,i2,i3]  # uses IndexListIterator
}</small></pre></blockquote>
***
<a name="hasNext"></a>
# hasNext
hasNext(  ) &rarr; boolean

true if there are more indeces in the iteration

### Returns:
true if there are more indeces in the iteration

<a href="https://github.com/autoplot/dev/search?q=hasNext&unscoped_q=hasNext">[search for examples]</a>

***
<a name="index"></a>
# index
index(  ) &rarr; int

return the current index.

### Returns:
the current index.

<a href="https://github.com/autoplot/dev/search?q=index&unscoped_q=index">[search for examples]</a>

***
<a name="length"></a>
# length
length(  ) &rarr; int

return the length of the iteration.

### Returns:
the length of the iteration.

<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>

***
<a name="nextIndex"></a>
# nextIndex
nextIndex(  ) &rarr; int

return the next index of the iteration

### Returns:
the next index of the iteration

<a href="https://github.com/autoplot/dev/search?q=nextIndex&unscoped_q=nextIndex">[search for examples]</a>


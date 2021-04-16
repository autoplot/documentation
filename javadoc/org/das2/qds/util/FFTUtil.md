# org.das2.qds.util.FFTUtilUtilities for FFT operations, such as getting the frequencies for each bin
 and fftPower.
FFTUtil( )


***
<a name="fft"></a>
# fft
fft( org.das2.qds.math.fft.GeneralFFT fft, QDataSet vds, QDataSet weights ) &rarr; QDataSet

Perform the fft to get real and imaginary components for intervals.

### Parameters:
fft - FFT code to use, such as GeneralFFT.newDoubleFFT(len)
<br>vds - QDataSet rank 1 dataset with depend 0 units TimeLocationUnits.
<br>weights - QDataSet rank 1 dataset containing weights, as in hanning.  null indicates no weights.

### Returns:
the rank 2 FFT

<a href="https://github.com/autoplot/dev/search?q=fft&unscoped_q=fft">[search for examples]</a>

fft( org.das2.qds.math.fft.GeneralFFT fft, QDataSet vds ) &rarr; Double<br>
***
<a name="fftPower"></a>
# fftPower
fftPower( org.das2.qds.math.fft.GeneralFFT fft, QDataSet vds ) &rarr; QDataSet



### Parameters:
fft - a GeneralFFT
<br>vds - a QDataSet

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=fftPower&unscoped_q=fftPower">[search for examples]</a>

fftPower( org.das2.qds.math.fft.GeneralFFT fft, QDataSet vds, QDataSet weights ) &rarr; QDataSet<br>
fftPower( org.das2.qds.math.fft.GeneralFFT fft, QDataSet vds, QDataSet weights, QDataSet powxTags ) &rarr; QDataSet<br>
***
<a name="getFrequencyDomainTags"></a>
# getFrequencyDomainTags
getFrequencyDomainTags( double fs, int size ) &rarr; double



### Parameters:
fs - the sampling frequency
<br>size - the size of the time domain data.

### Returns:
the frequencies of the bins

<a href="https://github.com/autoplot/dev/search?q=getFrequencyDomainTags&unscoped_q=getFrequencyDomainTags">[search for examples]</a>

getFrequencyDomainTags( QDataSet timeDomainTags ) &rarr; QDataSet<br>
***
<a name="getFrequencyDomainTagsForPower"></a>
# getFrequencyDomainTagsForPower
getFrequencyDomainTagsForPower( QDataSet dep0 ) &rarr; QDataSet

get the frequency tags, for use when calculating the power in each
 channel.  This removes the DC channel, and folds over the negative 
 frequencies.  This also keeps a cache for performance.

### Parameters:
dep0 - the timetags.

### Returns:
the frequency tags.

<a href="https://github.com/autoplot/dev/search?q=getFrequencyDomainTagsForPower&unscoped_q=getFrequencyDomainTagsForPower">[search for examples]</a>

***
<a name="getTimeDomainTags"></a>
# getTimeDomainTags
getTimeDomainTags( QDataSet frequencyDomainTags ) &rarr; QDataSet

return the time domain tags for inverse fft.

### Parameters:
frequencyDomainTags - a QDataSet

### Returns:
the time Domain Tags

<a href="https://github.com/autoplot/dev/search?q=getTimeDomainTags&unscoped_q=getTimeDomainTags">[search for examples]</a>

***
<a name="getWindow10PercentEdgeCosine"></a>
# getWindow10PercentEdgeCosine
getWindow10PercentEdgeCosine( int size ) &rarr; QDataSet

Window with ones in the middle, and then the last 10% taper with cos.

### Parameters:
size - the window size

### Returns:
window

<a href="https://github.com/autoplot/dev/search?q=getWindow10PercentEdgeCosine&unscoped_q=getWindow10PercentEdgeCosine">[search for examples]</a>

***
<a name="getWindowHanning"></a>
# getWindowHanning
getWindowHanning( int size ) &rarr; QDataSet

return a "Hanning" (Hann) window of the given size.

### Parameters:
size - an int

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getWindowHanning&unscoped_q=getWindowHanning">[search for examples]</a>

***
<a name="getWindowUnity"></a>
# getWindowUnity
getWindowUnity( int size ) &rarr; QDataSet

Window that is all ones, also called a boxcar.

### Parameters:
size - the window size

### Returns:
window

<a href="https://github.com/autoplot/dev/search?q=getWindowUnity&unscoped_q=getWindowUnity">[search for examples]</a>

***
<a name="ifft"></a>
# ifft
ifft( org.das2.qds.math.fft.GeneralFFT fft, QDataSet vds, QDataSet weights ) &rarr; QDataSet

Perform the inverse fft to get real and imaginary components for intervals.

### Parameters:
fft - FFT code to use, such as GeneralFFT.newDoubleFFT(len)
<br>vds - QDataSet rank 2 dataset with depend 0 units TimeLocationUnits and depend_1=['real','imaginary'].
<br>weights - QDataSet rank 1 dataset containing weights, as in hanning.  null indicates no weights.

### Returns:
the rank 2 FFT

<a href="https://github.com/autoplot/dev/search?q=ifft&unscoped_q=ifft">[search for examples]</a>

ifft( org.das2.qds.math.fft.GeneralFFT fft, QDataSet vds ) &rarr; Double<br>
***
<a name="window"></a>
# window
window( QDataSet ds, int size ) &rarr; QDataSet

returns a rank 2 dataset from the rank 1 dataset, where the
 FFT would be run on each of the datasets.

### Parameters:
ds - rank 1 dataset of length N
<br>size - size of each FFT.

### Returns:
rank 2 dataset[N/size,size]

<a href="https://github.com/autoplot/dev/search?q=window&unscoped_q=window">[search for examples]</a>


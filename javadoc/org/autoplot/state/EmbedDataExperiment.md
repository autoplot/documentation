# org.autoplot.state.EmbedDataExperimentEmbed data and vap in a zip file.  Now that we have PWD, this will
 be straight-forward.
EmbedDataExperiment( )


***
<a name="save"></a>
# save
save( org.autoplot.dom.Application dom3, java.io.File f ) &rarr; void

save the application, but embed data file resources within the 
 zip, along with the .vap.  The vap is saved with the name default.vap.
 When the data source contains a dataset that was created internally (with
 the Jython plot command, for example), it will be formatted as a QStream and 
 embedded within the vap.

### Parameters:
dom3 - the state to save.
<br>f - the zip file output name.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=save&unscoped_q=save">[search for examples]</a>


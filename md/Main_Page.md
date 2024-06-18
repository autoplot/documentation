<div id="launch" class="pBody" style="opacity:0.9;filter:alpha(opacity=90)">

![Logo96.png](Logo96.png "Logo96.png")

<span style="background-color:yellow;font-weight: bold;">[Start
Autoplot](http://autoplot.org/jnlp/latest/)&lt;/span&gt;&nbsp;
<span class="linuxnote" style="background-color:#ff99ff;display:none;">Linux
Installation</span>  
<span style="font-weight: bold;">[Start Devel
Version](http://autoplot.org/jnlp/devel/) </span>  
<span style="font-weight: bold;">[Installation](help.md#installation "wikilink")</span>  
<span style="font-weight: bold;">[Help](help.md "wikilink")</span>  
<span style="font-weight: bold;">[Screenshots](gallery.md "wikilink")</span>  
<span style="font-weight: bold;">[Cookbook](cookbook.md "wikilink")</span>  
<span style="font-weight: bold;">[Developer
notes](developer "wikilink")</span>

</div>

<table style="width:10%;">
<colgroup>
<col style="width: 4%" />
<col style="width: 6%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Getting Started</strong></p>
<hr />
<p>See the <a href="help" title="wikilink">help page</a> for usage instructions. Contact <a href="https://groups.google.com/forum/#!forum/autoplot">autoplot@groups.google.com</a> if you need assistance.</p>
<p><strong>About</strong></p>
<hr />
<p>Autoplot is an interactive browser for data on the web; give it a URL or the name of a file on your computer and it tries to create a sensible plot of the contents in the file. Autoplot was developed to allow quick and interactive browsing of data and metadata files that are often encountered on the web. For more information, see <a href="http://autoplot.org/wiki/images/autoplot.pdf">Faden et al. 2010</a> and introductory <a href="http://autoplot.org/wiki/images/autoplotIntroduction.ppt">PowerPoint</a>.</p>
<p><em>Autoplot was developed under the <a href="http://hpde.gsfc.nasa.gov/">NASA Virtual Observatories for Heliophysics</a> program in a collaborative effort among several institutions, including support or code contributions from <a href="http://virbo.org">ViRBO</a>, <a href="http://vmo.gsfc.nasa.gov">VMO</a>, <a href="http://www.rbsp-ect.lanl.gov/">RBSP-ECT</a>, and the <a href="http://www-pw.physics.uiowa.edu/">Radio and Plasma Wave Group at The University of Iowa</a>.</em></p></td>
<td><p><strong>Key Features</strong></p>
<hr />
<ul>
<li>Reads multiple ASCII formats including <a href="help#ASCII_table" title="wikilink">Complex ASCII tables</a>; <a href="help#Binary_table" title="wikilink">Binary tables</a>; <a href="http://cdf.gsfc.nasa.gov/">Common Data Format (CDF)</a>; <a href="http://www.unidata.ucar.edu/software/netcdf/ncml">NcML</a>; <a href="http://spase-group.org/">SPASE</a>; <a href="http://www.space-plasma.qmw.ac.uk/csds/welcome.html">Cluster Exchange Format</a>; <a href="http://www.unidata.ucar.edu/software/netcdf/">NetCDF</a>; <a href="http://opendap.org">OpenDAP</a>; <a href="http://www.hdfgroup.org/HDF5/">HDF5</a>; <a href="http://tsds.net">TSDS</a>; <a href="http://fits.gsfc.nasa.gov/fits_intro.html">FITS</a>; <a href="help#Excel" title="wikilink">Excel</a>; <a href="help#Wav_Files" title="wikilink">Wav</a>; <a href="help#Images" title="wikilink">PNG, JPG, etc</a>. For details and a full list, see <a href="help#Formats_Read" title="wikilink">Formats</a>.</li>
<li>Data is located with compact URI addresses. These contain the location of the data and additional information needed to use it.</li>
<li>Special support for <a href="help#CDAWeb" title="wikilink">CDAWeb server</a> at NASA/Goddard, <a href="http://hapi-server.org">HAPI</a>, and other data servers.</li>
<li><a href="https://das2.org">Das2</a> library used to create interactive graphics with slicing and custom interactions.</li>
<li>Wildcards can be used to <a href="help#Aggregation" title="wikilink">aggregate</a> (combine) data from multiple files into one time series.</li>
<li>Long time series may be rendered as a sequence of images as a <a href="PNG_Walks" title="wikilink">"pngwalk"</a> and viewed as a coverflow, table of thumbnails, or on a time line.</li>
<li>Any displayed data may be saved to disk in ASCII, <a href="http://cdf.gsfc.nasa.gov/">Common Data Format (CDF)</a>, and other formats, or plotted as PNG, PDF, or SVG.</li>
<li>GUI State may be saved as an XML <a href="developer.book#vap_files" title="wikilink">".vap"</a> file and restored.</li>
<li>Software may be run client side or <a href="https://cottagesystems.com/AutoplotServlet">server</a> side.</li>
<li>Data access layer for file reading may be used in <a href="matlab" title="wikilink"> MATLAB</a>, <a href="idl" title="wikilink"> IDL</a>, or <a href="python" title="wikilink"> SciPy</a> (via Java bridge), providing a common interface regardless of data source.</li>
<li><a href="https://github.com/autoplot/documentation/wiki/scripting">Scripting</a> via Jython, to control the application and read in data using metadata-aware datasets.</li>
<li><a href="http://autoplot.org/Autoplot_from_source">Open-source</a> (GPL with classpath exception) and may be used freely.</li>
</ul></td>
</tr>
</tbody>
</table>



<html>

<div>

<script type="text/javascript" src="//rf.revolvermaps.com/0/0/4.js?i=5gb0hgkpqgv&amp;m=0&amp;h=128&amp;c=ff0000&amp;r=0" async="async">

</script>

<script type="text/javascript">

rm2d\_ki101('5','200','100','5gb0hgkpqgv','ff0000',40);

</script>

</div>

<script>

$(document).ready(function () { $('\#launch \> p \>
a').attr('href','<http://autoplot.org/autoplot.jnlp>'); $('\#launch \> p
\> a').attr('title','Start Autoplot');
$('\#p-search').before($('\#launch'));
$('\#stats').append($('\#rm\_pkI1\_')); $('\#rm\_pkI1\_').wrap('

<div id="visitors" align="center" class="pBody">

</div>

'); $('\#visitors').prepend('Recent visits'); //$('\#visitors').hide();

// WebStart fix if ($.client.os == "Linux") {

```
 //$($(".external:contains('Start Autoplot')")).attr('href','`<http://autoplot.org/help#Installation>`').attr('Title','Linux operating system detected - link goes to special WebStart instructions');
```

}

```
   (function(h,o,t,j,a,r){
       h.hj=h.hj||function(){(h.hj.q=h.hj.q||[]).push(arguments)};
       h._hjSettings={hjid:1307322,hjsv:6};
       a=o.getElementsByTagName('head')[0];
       r=o.createElement('script');r.async=1;
       r.src=t+h._hjSettings.hjid+j+h._hjSettings.hjsv;
       a.appendChild(r);
   })(window,document,'`<https://static.hotjar.com/c/hotjar->`','.js?sv=');
```

});

</script>

</html>




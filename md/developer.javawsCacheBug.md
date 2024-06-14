I thought I'd try to figure out the caching bug that we see with
Autoplot but not with jnlp apps released on the das2 website.

# Note

I tried the jnlp link here

<http://autoplot.org/jnlp/v2012b_8/>

and watched the log files. It appears that webstart never makes a new
head request to the server. Do you have an example jnlp that works the
way that you want it to?

In other news, see the section "Using the DownloadService Service" at
<http://docs.oracle.com/javase/6/docs/technotes/guides/javaws/developersguide/examples.html>

See also the discussion at (in particular the part about the new
behavior in WebStart regarding start-up)
<http://stackoverflow.com/questions/10387464/delete-java-jar-from-cache-after-execution>

It would seem that a possible solution is for you to symlink

AutoplotVolatile.jar to AutoplotVolitale-VERSION.jar.

# Update issues

The problem: I can't push new versions of the software to people from
the autoplot.org website. Once a release is made and the user downloads
it, javaws will not reload the app jars again even if their timestamps
change. The user must uninstall then reinstall the application to get an
update. Because of this, we always change the name of the releases.

## Experiment on www-pw

I do a first release...

```
/home/jbf
```
`klunk$&nbsp;javaws&nbsp;`&lt;http://www-pw.physics.uiowa.edu/das2/apps/autoplot-juno.jnlp&gt;  
  
```
/home/jbf
```
`klunk$&nbsp;curl&nbsp;--head&nbsp;`&lt;http://www-pw.physics.uiowa.edu/das2/apps/autoplot-juno.jar&gt;  
```
HTTP/1.1 200 OK
Date: Wed, 04 Jan 2012 20:50:51 GMT
Server: Apache/2.2.13 (Unix) DAV/2 PHP/5.2.11 mod_fastcgi/2.4.2 mod_perl/2.0.3 Perl/v5.8.8
Last-Modified: Mon, 06 Jun 2011 15:02:55 GMT
ETag: "c081-1396888-4a50c65ed76b4"
Accept-Ranges: bytes
Content-Length: 20539528
Content-Type: text/plain
```

I touch the jar file and use javaws to run the app. I can see it
reloading the jar file.

```
/home/jbf
```
`klunk$&nbsp;javaws&nbsp;`&lt;http://www-pw.physics.uiowa.edu/das2/apps/autoplot-juno.jnlp&gt;  
  
```
/home/jbf
```
`klunk$&nbsp;curl&nbsp;--head&nbsp;`&lt;http://www-pw.physics.uiowa.edu/das2/apps/autoplot-juno.jar&gt;  
```
HTTP/1.1 200 OK
Date: Wed, 04 Jan 2012 20:51:29 GMT
Server: Apache/2.2.13 (Unix) DAV/2 PHP/5.2.11 mod_fastcgi/2.4.2 mod_perl/2.0.3 Perl/v5.8.8
Last-Modified: Wed, 04 Jan 2012 20:51:04 GMT
ETag: "c081-1396888-4b5b9f9632dec"
Accept-Ranges: bytes
Content-Length: 20539528
Content-Type: text/plain
```

## Experiment on autoplot.org

```
/home/jbf/
```
`klunk$&nbsp;curl&nbsp;--head&nbsp;`&lt;http://autoplot.org/jnlp/v2011a_5/AutoplotVolatile.jar.pack.gz&gt;  
```
HTTP/1.1 200 OK
Date: Wed, 04 Jan 2012 20:40:58 GMT
Server: Apache/2.2.14 (Ubuntu)
Last-Modified: Wed, 04 Jan 2012 20:40:55 GMT
ETag: "41002a-17d17f-4b5b9d50fc3c0"
Accept-Ranges: bytes
Content-Length: 1560959
Cache-Control: max-age=31536000
Expires: Thu, 03 Jan 2013 20:40:58 GMT
Content-Type: application/x-gzip
```

And after touching the file on the server...

```
/home/jbf
```
`klunk$&nbsp;curl&nbsp;--head&nbsp;`&lt;http://autoplot.org/jnlp/v2011a_5/AutoplotVolatile.jar.pack.gz&gt;  
```
HTTP/1.1 200 OK
Date: Wed, 04 Jan 2012 21:12:14 GMT
Server: Apache/2.2.14 (Ubuntu)
Last-Modified: Wed, 04 Jan 2012 21:12:11 GMT
ETag: "41002a-17d17f-4b5ba44e140c0"
Accept-Ranges: bytes
Content-Length: 1560959
Cache-Control: max-age=31536000
Expires: Thu, 03 Jan 2013 21:12:14 GMT
Content-Type: application/x-gzip
```

# Desktop icon issues

**Experiment 0**

OS X 10.6.8

(Note - I just ran through this again after deleting all of the icons
and closing all Autoplot's and I get different results\!)

When I do

<http://autoplot.org/autoplot.jnlp?version=hudson>

I get an icon on the desktop and the application launches normally.

When I click on the desktop icon after closing, I get

CouldNotLoadArgumentException\[ Could not load file/URL specified:
<http://autoplot.org:8080/hudson/job/autoplot-release/130/artifact/autoplot/VirboAutoplot/dist/AutoplotVolatile.jarjnlp>

If I then do

<http://autoplot.org/autoplot.jnlp?version=hudson>

it asks to put an icon on the desktop again.

When I do

<http://autoplot.org:8080/hudson/job/autoplot-release/lastSuccessfulBuild/artifact/autoplot/VirboAutoplot/dist/autoplot.jnlp>

I get asked to put an icon on the desktop, but one never appears.

When I do

<http://autoplot.org/autoplot.jnlp>

I don't get an icon on the desktop. Same if I try

<http://autoplot.org/jnlp/v2012a_4/autoplot.jnlp>

If I do

<http://autoplot.org/autoplot.jnlp?version=hudson&mode=basic&open=bookmarks:http://autoplot.org/bookmarks/heliophysics.xml>

I get asked to put an icon on the desktop and I can click on the desktop
to have Autoplot launch normally (but it asks me again if I want to put
it an icon on the desktop).

**Experiment 1** On Mac + Chrome, click

<http://autoplot.org/jnlp/v2011a_9/autoplot.jnlp>

and an icon appears on the desktop. After closing, clicking on icon
starts Autoplot with no "save as" prompt. On a fresh install of Windows
7 + FF 10, I get "What should Firefox do with this file?" and a dialog
with no option to open as Java WebStart. After going to
<http://java.com/en> and clicking "Free Java Download" I get "Open with
Java(TM) Web Start Launcher (default)" and a desktop icon that starts
Autoplot with no "save as" prompt.

Delete the desktop icon and click

<http://autoplot.org/jnlp/v2011a_9x/autoplot.jnlp>

(jnlp has no href). On Mac + Chrome, no icon appears on desktop. On FF
10 + Windows 7 + Java 1.6.0\_31, I get a desktop icon; closing Autoplot
and clicking desktop icon does not result in a "save as" prompt. (Note
that Autoplot still appears as an installed program after the desktop
icon is deleted.)

Now click

<http://autoplot.org/jnlp/v2011a_9/autoplot.jnlp>

and no icon appears on desktop\!

**Experiment 2**

<http://lopica.sourceforge.net/faq.html> "One trick is to make sure not
to include the href attribute in the JNLP file that your servlet sends
back to Web Start. This will tell Web Start to disable the update check
on JNLP files, and Web Start will not treat each new JNLP file as an
application update - only updated jar files will."

This link creates a jnlp with the href as autoplot.jnlp instead of it
being removed:

<http://autoplot.org/cgi-bin/autoplot_keep_href.jnlp>

**Experiment 3** All of the following return the same jnlp file. None
result in icon on desktop on Mac + Chrome.

```
wget` saves as `jnlp2.cgi
```

`curl&nbsp;-I&nbsp;`&lt;http://autoplot.org/cgi-bin/jnlp2.cgi&gt;  
  
```
HTTP/1.1 200 OK
Date: Sat, 25 Feb 2012 15:14:45 GMT
Server: Apache/2.2.14 (Ubuntu)
Content-disposition: attachment;filename="autoplot.jnlp"
Cache-control: no-cache, no-store, must-revalidate
Content-Type: application/x-java-jnlp-file
```

```
wget` saves as `autoplot.jnlp
```

`curl&nbsp;-I&nbsp;`&lt;http://autoplot.org/cgi-bin/autoplot.jnlp&gt;

```
HTTP/1.1 200 OK
Date: Sat, 25 Feb 2012 15:38:30 GMT
Server: Apache/2.2.14 (Ubuntu)
Content-disposition: attachment;filename="autoplot.jnlp"
Cache-control: no-cache, no-store, must-revalidate
Content-Type: application/x-java-jnlp-file
```

```
wget` saves as `autoplot_attachment.cgi
```

`curl&nbsp;-I&nbsp;`&lt;http://autoplot.org/cgi-bin/jnlp_attachment.cgi&gt;  
  
```
HTTP/1.1 200 OK
Date: Sat, 25 Feb 2012 15:26:46 GMT
Server: Apache/2.2.14 (Ubuntu)
Content-disposition: attachment;filename="autoplot.jnlp"
Cache-control: no-cache, no-store, must-revalidate
Content-Type: application/x-java-jnlp-file
```

```
wget` saves as `autoplot_no_content_disposition.cgi
```

`curl&nbsp;-I&nbsp;`&lt;http://autoplot.org/cgi-bin/jnlp_no_content_disposition.cgi&gt;  
  
```
HTTP/1.1 200 OK
Date: Sat, 25 Feb 2012 15:27:56 GMT
Server: Apache/2.2.14 (Ubuntu)
Cache-control: no-cache, no-store, must-revalidate
Content-Type: application/x-java-jnlp-file
```

```
wget` saves as `autoplot_inline.cgi
```

`curl&nbsp;-I&nbsp;`&lt;http://autoplot.org/cgi-bin/jnlp_inline.cgi&gt;  
  
```
HTTP/1.1 200 OK
Date: Sat, 25 Feb 2012 15:25:39 GMT
Server: Apache/2.2.14 (Ubuntu)
Content-disposition: inline;filename="autoplot.jnlp"
Content-Type: application/x-java-jnlp-file
```


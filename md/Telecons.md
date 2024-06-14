# January 15, 2010

  - Bob mod addHTML extension to allow editors to addhtml
  - Install packages (Do as part of late spring release)
  - Pack gz - What a state things are in. Here's the version that uses
    the pack200/gz stuff:
    <http://autoplot.org:8080/hudson/job/autoplot-jar-volatile/>... We
    are using the pack200 and gzip here, it's just the proguard stuff we
    dropped. I can see it's commented out here:
    <http://autoplot.org:8080/hudson/job/autoplot-jar-volatile/ws/autoplot/VirboAutoplot/compile-application-two-jars.sh/*view*/>
    (Jeremy - merge into production release very soon)
  - Jeremy contact Ed about Jan 15th email and bulleted list
  - Don't worry about png - will use Jquery autoload on scroll tool to
    make page not bog down.
  - Bob move videos to help (done)
  - Issue for Ubuntu 9.04 - Bob do probe of OS and warn user near link
  - Discuss repository - Jeremy review and email Bob - no response from
    Jon?
  - Bookmarks - Bob modify

# Nov. 23, 2009

  - Need to start an outline for a book
  - Need to write demo scripts for IDL and MATLAB that export data and a
    jnlp file that can be posted to web

# October 23, 2009

# October 2, 2009

  - To do before new production version
      - WebStart - Need to add pack.gz (hour of searching around
        required)
      - Bookmarks - make sure every feature is highlighted
      - Documentation - make sure interaction is documented (if first
        use, give option to show user interaction which points to a
        link)

# August 20, 2009

  - Q: Is there an option in das2 for setting the number of colors in
    the colorbar and the bin size? That is, can I make 0-1 white, 1-2
    green, etc? A: Sounds like a custom renderer to me. Another thing
    we've talked about is adding to the set of color tables to include
    16-color ones with discrete steps, and color bars that are more
    friendly to colorblind people.
  - Q: NCML for multiple time axes. A: Yes, this needs to get done.
    Should be pretty easy to do, but we should decide if it's just going
    to be a capability, or if it should be a core feature of autoplot.
    For example, in PaPCO it's almost a core feature where all the
    modules can expect that a service to provide ephemeris for a set of
    spacecraft is available. For das2 my plan has been to make it
    spacecraft-aware in the same sense that it is units aware. So for
    example a time axis would know that it's a time axis for ACE, and it
    knows how to go find ephemeris, and one of the axis mouse modules
    displays the S/C position with respect to the Earth and Sun, etc.
  - Q: Perhaps we should define a way of using NCML to specify a
    colorbar. A: That's a hairy place where you've got a data model
    trying to do display stuff. I already have mixed feelings about
    adding "RENDER\_TYPE=stairsteps" to the output of autohistogram.
    Probably the best thing is to have a detailed spec of the display
    with a good identifier ("bobsColorMap") and allow the data model to
    gently request it ("with RENDER\_TYPE=bobsColorMap"). Jon and I
    finally have a visit planned on October, and then we'll be able to
    start building up the dataset schemas. Then Autoplot can have
    sophistocated logic for mapping scheme type
    (rank2table\>spectrogram\>discretemap\>bobsdescretemap) to render
    type (bobsColorMap). I think this is probably the cleaner way to do
    things...
  - Discuss what is required before release - what parts listed at
    <http://www.sarahandjeremy.net/jeremy/mediawiki-1.6.9/index.php/Autoplot_todo#Aaron.27s_Comments>
  - Applet - Keep proguard in build script, but don't use because needs
    debugging and we are already down to 400 KB with refactoring.
  - To do before new production version
      - WebStart - Need to add pack.gz
      - Bookmarks - make sure every feature is highlighted
      - Bookmarks - create bookmarks-testing.xml from wiki page
      - Document rendering
      - Documentation - make sure interaction is documented
      - Fix slicing problem -- high rank datasets sliced by panel before
        display, affects DOM.
      - Fix serialization issue -- use custom xml serializer instead of
        Java's?
      - Fix/address back and forward compatible DOM issues
      - Applet clean up right-click
      - Applet reset zoom
  - Minor:
      - progress panel smarter about popup.

# July 10, 2009

  - Move js/order/autoplotform\* to demo page for servlet. Need servlet,
    applet, and webstart to each have their own release and demo pages\!
  - <http://autoplot.org/api> What about canvas.aspect?
  - Discuss fullscreen <http://aurora.gmu.edu/svn/js/applet>
  - Discuss Ed working on event list creator
  - Discuss Ed working on dir reader applet
  - Create AutoplotAppletCompressed.html and htaccess.txt. The html file
    should tell the user that if they downloaded the release they will
    need to rename htaccess.txt to .htaccess.
  - Put in webstart instructions for apache mime type config.

# July 2, 2009

  - Jeremy finish API page ASAP
  - Bob will commit new html to applet directory
  - Much discussion about the following. Bob wants a simple thing that
    allows a callback to be registered to Javascript when the user
    clicks on the canvas. The callback function will get a string with
    the time and X,Y,Z coordinates. There was discussion on how to best
    do this in the more formal way. No conclusion was reached.

> I just had an idea, inspired by something I was about to do in MATLAB
> for a research problem that I am working on. While browsing a time
> series, select "Create Event List". When the user clicks on a
> location, a textbox is populated in another window  
> Start: 2009-01-01  
> the next click leads to this showing up below the text window  
> End: 2009-01-01  
> Note1:  
> The next click leads to the addition of another Start line. And so
> on.  
> User may hand-edit the text in the window. They may add as many NoteX
> lines as they want. They may also select among a few output formats:  
> SPASE:  
> <http://virbo.org/meta/viewdata.do?docname=D2FA2398-EA13-95D4-E8AE-C97D97CF987C>  
> Flat file:  
> YYYY MM DD DOY Note

# May 22, 2009

  - Should axis re-set on scan? I think it should. We would need a
    setting to not enable autoscale then.
  - Discuss API page
  - Test that applet and servlet are accepting all parameters the same
    way

# May 6, 2009

  - Action items for next week
      - Create examples for existing version of applet on how to control
        properties after initial load.
      - Find write-up from our filter API discussion when I was there. I
        can't find it.
  - Action item for before next release: Test and integrate
    <http://aurora.gmu.edu/svn/js/order/autoplotform>.\* into Autoplot
    code tree
  - Action item for before next release: Create
    <http://autoplot.org/api> (has DOM plus example of how to modify one
    element in the DOM. For help on the meaning of DOM node, user is
    pointed to <http://autoplot.org/help>
  - Data set plugin with URI or DOM inputs of data discussed as future
    feature.
  - EMFISIS is using Autoplot to have first look at raw data coming off
    of the instrument. Create a list of "users" on the autoplot main
    page?
  - Send Vandergriff email and ask to try Eclipse? Wait till next
    version is out.
  - Discuss how we will handle release that require pack200 and ... I
    was thinking that it was weird that we were using Unix shell scripts
    to call java programs instead of using ant.
  - Senior review draft was discussed. No action item.
  - I think that we should maintain a separate Telecon wiki page for
    notes like these. Done.


Autoplot needs a local space to run the full application. This is in
$HOME/autoplot\_data/, so it is at:

  - /home/$USER/autoplot\_data on linux/unix
  - /Users/$USER/autoplot\_data on a mac and Windows 7
  - C:\\Documents and Settings\\USER\\autoplot\_data on Windows XP

Within this folder there are the folders:

  - fscache/ area for the cache of downloaded files
  - plugins/ jar files for new plugins go here, also
    jython-implementations of plugins. These are not used because of
    Webstart security. For local installations, this probably still
    works.
  - bookmarks/ bookmarks storage and recent links.
  - tools/ Jython scripts that are added to the menu bar under tools.
  - pycache/ Python puts stuff here for its operation

The fscache can be moved using the Autoplot GUI to a different
filesystem.

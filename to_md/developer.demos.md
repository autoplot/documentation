Purpose: Notes for demos

Audience: Scientists and autoplot developers

# scripting to get metadata for a pile of files

Sarah had a nice use case where she had a bunch of .wav recordings and
needed to figure out which files had been recorded in 32 bits.

1.  copy over the files to the local drive
2.  short jython script to load in each file and get the metadata.
3.  monitor shows progress for each one. The files could be on a remote
    site.
4.  the results are printed. Python formatting.
5.  the directory name appears twice in the script. fix this with a
    variable.
6.  we might want to do this for any directory, add a getParam call.
7.  add this to the Autoplot Tools menu.
8.  documentation string

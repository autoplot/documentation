Purpose: outline how to set up Git on a Mac.

1. git appears to be installed out of the factory.  Verify this with "git" at the command line.
2. set up public/private keys with ssh-keygen
3. copy the PUBLIC key to github/gitlabs.  This is /home/jbf/.ssh/id_rsa.pub  (Guard id_rsa carefully.  This is the security.)
4. git clone git@github.umn.edu:FADEN004/talk_20210928.git
5. Now start up Autoplot, where we will add the git commands.
6. on Script tab, right-click, Settings->Editor Bookmarks
7. Edit->New Folder...
8. https://raw.githubusercontent.com/autoplot/dev/master/demos/tools/editor/git-actions.xml. (Note this is the "raw" version, because the normal github version doesn't work.  This is a bug which will be fixed.)
9. Linking github remote site to local repository
10. How to collaborate with others using a private repository.

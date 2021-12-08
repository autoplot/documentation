Purpose: outline how to set up Git on a Mac.

1. what is git?
   - look at https://github.com/autoplot/dev/
   - enter the location into Autoplot and it will run the script immediately.
   - this works for *public* repositories which anyone can access.
2. what about private git repos?
   - log into github.com and show https://github.com/autoplot/private_study
   - only people I share this repo with can see the files, or even the folder itsself.
   - Autoplot hasn't been able to use these repos until recently.
4. I'll show how to use such repos in Autoplot and its new support for command-line git use.
5. git appears to be installed out of the factory.  Verify this with "git" at the command line.
6. set up public/private keys with ssh-keygen
7. copy the PUBLIC key to github/gitlabs.  This is /home/jbf/.ssh/id_rsa.pub  (Guard id_rsa carefully.  This is the security.)
8. git clone git@github.umn.edu:FADEN004/talk_20210928.git
9. Now start up Autoplot, where we will add the git commands.
10. on Script tab, right-click, Settings->Editor Bookmarks
11. Edit->New Folder...
12. https://raw.githubusercontent.com/autoplot/dev/master/demos/tools/editor/git-actions.xml. (Note this is the "raw" version, because the normal github version doesn't work.  This is a bug which will be fixed.)
13. Linking github remote site to local repository
14. How to collaborate with others using a private repository.

Purpose: outline how to set up Git on a Mac.

# First video
The first video introduces git and how it can be used with Autoplot scripts.

1. what is git?
   - look at https://github.com/autoplot/dev/
   - enter the location into Autoplot and it will run the script immediately.
   - strike decorator at https://github.com/autoplot/dev/blob/master/demos/annotations/strike/strikeDecorator.jy
   - this works for *public* repositories which anyone can access.
2. what about private git repos?
   - log into github.com and show https://github.com/autoplot/private_study
   - only people I share this repo with can see the files, or even the folder itsself.
   - Autoplot hasn't been able to use these repos until recently.
4. I'll show how to use such repos in Autoplot and its new support for command-line git use.
5. git appears to be installed out of the factory.  Verify this with "git" at the command line.
6. set up public/private keys with ssh-keygen
7. copy the PUBLIC key to github/gitlabs.  This is /home/jbf/.ssh/id_rsa.pub  (Guard id_rsa carefully.  This is the security.)
8. git clone git@github.com:autoplot/private_study.git  Note my cable internet blocked port 22!  h
9. make a trivial change, show git diff, commit.
10. give a peek at Autoplot's script, and the diff action.

# Second video
1. Now start up Autoplot, where we will add the git commands.
2. on Script tab, right-click, Settings->Editor Bookmarks
3. Edit->New Folder...
4. https://github.com/autoplot/dev/blob/master/demos/tools/editor/git-actions.xml.
5. Linking github remote site to local repository.  New script "linkToUpstream" does this.
6. How to collaborate with others using a private repository.

Purpose: outline how to set up Git on a Mac.

# First video
The first video introduces git and how it can be used with Autoplot scripts.

1. what is git?
   - look at https://github.com/autoplot/dev/
   - enter the location into Autoplot and it will run the script immediately.
   - strike decorator at https://github.com/autoplot/dev/blob/master/demos/annotations/strike/strikeDecorator.jy
   - this works for *public* repositories which anyone can access.
2. what about *private* git repos?
   - log into github.com and show https://github.com/autoplot/private_study
   - only people I share this repo with can see the files, or even the folder itsself.
   - Autoplot hasn't been able to use these repos until recently.
4. I'll show how to use such repos in Autoplot and its new support for command-line git use.
5. git appears to be installed out of the box.  Verify this with "git" at the command line.
6. set up public/private keys with ssh-keygen
   - if you already have ~/.ssh/id_rsa.pub, you can just use this file.
   - Use the default if you don't have the file ~/.ssh/id_rsa.pub
   - passphrase cannot be used, as there's no way to enter a passphrase.
8. copy the PUBLIC key to github/gitlabs.  This is ~/.ssh/id_rsa.pub  (Guard id_rsa carefully.  This is the security.)
9. git clone git@github.com:autoplot/private_study.git  Note my cable internet blocked port 22!  
10. make a trivial change, show git diff, commit.
11. give a peek at Autoplot's script, and the diff action.

# Second video
New actions in the Autoplot script editor.

1. Now start up Autoplot, where we will add the git commands.
2. on Script tab, right-click, Settings->Editor Bookmarks
3. Edit->New Folder...
4. https://github.com/autoplot/dev/blob/master/demos/tools/editor/git-actions.xml.
5. Linking github remote site to local repository.  New script "linkToUpstream" does this.
6. How to collaborate with others using a private repository.

# Third video 
The third video shows how collaboration is done with multiple people working on an area.

1. Note that local repo overrides what's on the upstream site
   - You have to be aware if things haven't been committed.
   - You need to pull to see changes your colleague has made
2. Let the remote site be the authority, since it shows what is actually upstream.
3. What to do when there are conflicts.
4. xkcd cartoon has it right--just move the old one out of the way and clone a new one.
5. pull before you push

# Fourth Video
Use case where github is used to store digitized data set.

1. introduce digitizing task
2. when done for the day
   - pull to get other's commits
   - commit and push your changes
3. review the github site

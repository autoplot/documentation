Audience: Autoplot users looking to store credentials for convenience and to allow
scripting.

# Introduction
Autoplot uses Das2 Filesystem abstraction to allow access to remote files the same
as if they were local.  Often http-based filesystems require a password so that 
groups can manage data before they are ready for the public.  When these use
http authentication, the Das2 Filesystem will present a credentials dialog, which
allows the password to be stored in a keychain.txt file for future automatic 
use.

<img width="744" height="630" alt="image" src="https://github.com/user-attachments/assets/2dbffdb5-95f5-4b12-9025-18d47742dc49" />

# Implementation
The passwords are stored in the fscache at HOME/autoplot_data/fscache/keychain.txt.  Access to this file is limited
to the scientist, and the file contains the website, then the user:password combination to use with the site.

# GitHub/GitLab Filesystems
GitLab and GitHub filesystems allow access to private repositories when a "token" is used.  This is a long
string of letters and numbers generated on the website, which can be used to provide colleagues with
access to the filesystems.

<img width="720" alt="image" src="https://github.com/user-attachments/assets/d2a97d7c-fc31-4a3e-944e-418946402dc7" />

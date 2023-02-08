Autoplot is not written by a large software company with many programmers and a team that
validates every release.  It's written mostly by one person, and the primary goal is to
do science, and we will get great software out of the effort as well.  So you should not
be discouraged if you encounter bugs, and when bugs are reported they are usually fixed
quickly.

This describes the process of what happens when a bug is reported, and what you can do
to make this as easy a task as possible.  When the task is easy for the developers, the
bug will be fixed more quickly, so it's in everyone's interest.

If a bug is reported, the first thing the developer must do is to be able to demonstrate
the bug.  If we can't see it, there's almost no way we can fix it.  Ideally, you would
send .vap which when run, shows the bug.  A URI containing a public-facing data file 
is also helpful.  When that won't work, a short description of how to show the bug, including
a step-by-step procedure to follow, should be provided.  Last, when the data is not on
a public-facing website, a .vap file can be created with the "embed data" checkbox 
selected.  This will save the usual .vap file along with the data files in a .vap.zip file
which the developer can open.  Last, we understand that often data is unpublished or even
secret, and if possible, a similiar dataset which shows the same bug is useful.  Ultimately
we want to help you to fix the problem.  It's likely others are affected by the same bug,
and by reporting the bug, even without any supporting data, will help the broader community.

After the bug is demonstrated, the developer will likely run Autoplot where we can debug
the code, adding breakpoints which pause excution and allow us to see what's going on "under
the hood."  Java provides sophistocated tools which allow problems to be quickly diagnosed
and resolved.  

When the case which demonstrates the bug is fixed, the code changes are committed to the repository
along with information about the changes.  More complex bugs will often have a "bug ticket" which
documents the bug and the resolution.  (When a bug ticket is started, the scientist will get a link
to the ticket so they can see progress towards the bug's resolution.)  A new version can 
then be built, creating a "nightly build" release which can be delivered to the scientist 
reporting the bug, when they need a corrected version of Autoplot quickly.

At this point the scientist may think the process is done, but it is not.  Bugs tend to emerge
around the same poorly-engineered code, so it is important to put the bug into regression testing.  Regression
is when a fixed bug is broken again.  This can happen when two features contradict one another, and
it is impossible to provide both functions, but that's a worst-case.  The .vap file may be added to the tests or the
step-by-step instructions are coded as a jython script which runs regularly.

Last, we have to make sure other features have not been affected, and the end-to-end testing is run
again.  This takes about 30-60 minutes right now.  When all the tests are running okay, a new development release is
made.  The goal there is to have a new development release (e.g. 20230208a) within each week.  Production 
releases (e.g. v2023a_2) are made roughly once a month, and are only made when there is high-confidence that
no new bugs have been introduced.



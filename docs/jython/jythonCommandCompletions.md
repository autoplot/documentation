When completions are triggered on the plot command, a static 
page is shown.  It would be nice to allow for completions on keywords 
with documentation explain use.

Now if the Jython command has the tags `__completions__`, it will be a string which
is parsed as JSON.  This JSON explains each keyword.


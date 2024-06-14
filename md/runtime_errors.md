When Runtime Errors occur, the errors are caught and the scientist can
send them in to the developers. This allows people who are not in
regular contact with us to have their problems fixed. This has been
incredibly effective for quickly identifying and resolving new errors in
the software, and we encourage everyone using Autoplot to submit errors.

When the dialog pops up, the scientist may add additional comments and a
screenshot, and the result is uploaded to a server which accepts the
report. The dialog shows what will be submitted. The submission will
contain the state of each of the many threads of execution, a vap
showing the current state, undo information to show what lead to the
runtime error, and the current entry in the address bar.

The scientist may also add an email address so that we may contact them
for more information.

# Privacy

We all work with a common interest, but scientists should consider what
information is revealed.

Note locations of data used are found within the file, and references to
locations on your hard drive are left in the vap. Undo history is found
within the file. The scientist's username is included. Last, the IP from
which the submission is made is revealed. The text which will be
submitted can be found on the dialog, or by saving to a local file.

When a screenshot is made for the submission, a mask is applied to hide
all non-Autoplot windows, but this process may sometimes miss borders
and include data from another window.

The scientist's username may be acknowledged in the releases. For
example, the release may remark the issue along with the submitter's
username: "New issue with aggregation corrected. Thanks Jonny\!" The
goal here is that the scientist (Jonny in this example) is able to see
that their issue has been addressed.

# Unpacking the Screenshot

The screenshot is base64-encoded within the XML which is sent in. To
extract the image, grep for part of the text in the encoded image, so
that just that line is extracted, then pipe it through base64:

```
cat rte_0335135088_20230203_120506_jonny.xml | grep 0aJjaou+Us | base64 --decode > 20230223_120506.png
```

# Provide Feedback

The menu item Help &rarr; &quot;Provide Feedback&quot; uses the same mechanism to
submit feedback.


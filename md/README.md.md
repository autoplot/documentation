The goal here is to study migrating the mediawiki content to github or
similar.

Much content was created on autoplot.org, which is a mediawiki-based
website. I know I have other places where I have converted mediawiki
content to markdown, and I expect I'll do that to the entire site.

pandoc looks like its a useful tool. For example:

\`pandoc -f mediawiki QFunction -t markdown\_github -o QFunction.md\`

converts the one file, but does a poor job with code blocks. I've
written an Autoplot script to clean this up.

\`pandoc -f html <http://autoplot.org//QFunction> -t markdown\_github -o
QFunction.md\`

downloads the mediawiki page and writes directly to markdown. It looks
like with a little massaging (removing head and tail) this would work
nicely.

1.  20220723

Bob mentioned at some point mediawiki will come down. I rarely use it,
but I just found myself using it this morning, so I thought I should
reload the changes to here. The script for downloading things is here
<https://github.com/autoplot/dev/tree/master/demos/2020/20201014/>

1.  2024-06-11

I'm picking this up again after Autoplot was down for a few days while
Bob and I were both on vacation. Plus this is way overdue.

\`pandoc -f mediawiki QFunction -t markdown\_github -o QFunction.md\`

looks like the best way to go, and then I need to find the script which
does clean up after.


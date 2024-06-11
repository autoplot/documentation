Audience: Autoplot power users needing more information about what's
changed with Autoplot 2017.

# Introduction

Autoplot has always had the name "virbo" in its package names, as it was
begun as a component of this VxO project. It has since taken on a life
of its own, and for years we've intended to remove virbo references in
the code. However, there are a number of technical challenges to this:

  - Jython Scripts often contain imports with the virbo package name.
  - Launcher scripts, external to Autoplot's .jnlp release, use the
    virbo name.
  - Matlab and IDL use a bridge with the path name.
  - Autoplot .vap files contain references to virbo.

However we have also planned on moving QDataSet maintenance to the RPW
Group at the University of Iowa, and with this giant change we might as
well get all the package name changes done at once. This will be the
2017a branch.

Legacy scripts will be supported by refactoring the script prior to
execution. Launchers will be included that support legacy calls. We all
have plenty to think about, to suddenly have Autoplot causing problems,
and our hope is that this change will be seamless and you can continue
to get real science done.

Anyone directly linking to Autoplot code can request help with the code
changes at autoplot@groups.google.com.

# What to do when you see the message "reference to old org.virbo.autoplot needs fixing"

Look at your script, and you should be using org.autoplot.X instead of
org.virbo.autoplot.X. Note this means that older Autoplot installations
will not be able to use the script, so do so carefully. Many people can
not easily control which version of Autoplot they are using.

# See Also

<https://sourceforge.net/p/autoplot/feature-requests/528/>

Audience: Autoplot and das2 developers

Purpose: Explain use and lifecycle of progress monitor objects.

# Introduction

The definition of proper management of monitor objects has moved around
over the years, and after discovering Autoplot bug
<https://sourceforge.net/p/autoplot/bugs/1251/> and realizing I've lost
my documents on how to manage progress monitors, I realized this needs
to be documented again.

# Lifecycle

  - Either the progress monitor is ignored, or
  - all uses of the progress monitor are within one script or Java code.

So the lifecycle goes like this:

  - monitor.setTaskSize(int) is the size is determinate.
  - monitor.started() is called.
  - repeat any number of times:
      - monitor.setTaskProgress(int) is called. Monitors must be careful
        because this method may be called millions of times a second,
        and it must be quick.
      - monitor.setProgressLabel(String) is called.
  - monitor.finished is called. Just once\!\!\!\!


Purpose: outline small projects that could be done by programmers in the
community.

Audience: developers interested in contributing to Autoplot

# Introduction

Autoplot is an open source project, but there's quite a learning curve
to climb before getting involved. This document hopes to outline some of
the smaller projects that could be performed without an understanding of
the system as a whole.

# Particular Projects

## science demos (2012-04-27)

We have a constant need for people to provide science demos showing
Autoplot doing some real work. I take screenshots as I debug, but
typically this is to test a part of the system and the plots itself is
not very interesting. There's a script that automatically takes
screenshots as you work, which can be useful for story boarding a demo.

# Milestones

Collect the feature sets that will highlite each version. Note minor
features that don't break a version may be introduced before the
release.

## 2013b

  - filters in URIs, for example, add a slice to the dataset.
    (Seth,Jeremy,Reiner)
  - ISO8601 used to store timeranges, timeranges as strings, not
    objects. renderType, colorbar, units, etc as string not object. All
    of this is to make extension easier. All property nodes are
    string,float,or int. v1.08 vap file. (Jeremy,Bob)
  - improvements to jython completions and getParam. (Bob,Jeremy, and
    many others affected by this.)
  - study and fix the problem where timeranges in URIs remove control
    from the user. For example, query the user to make sure this is what
    they intended. (Jeremy,Bill,Craig,Reiner)
  - "now" in timeranges (DONE)
  - Message Bubbles turned off when printing, easy for users to
    acknowledge, possibly dissappear after so many seconds.
  - data reduction during load of agg data source.

## 2014a

  - where comes up a lot. Show me this parameter where this other
    parameter gt,lt,eq,etc x. (Seth,Jeremy)
  - semanticOps and other cleanup of jython scripts. (Bob,Jeremy, and
    many others affected by this.)
  - proper units handling.

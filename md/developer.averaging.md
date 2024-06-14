Purpose: Describe aspects of combining data. Audience: Scientists and
software developers.

# Introduction

Things start getting tricky when you start to combine data. For example,
if you wish to combine the measurements made over an hour, this might be
typically done by averaging all the measurements together. But consider
that software might be doing this with any data without human guidance,
and the data might be a flag indicating data quality. In this case
averaging 0=ok with 1=bad to get 0.5 doesn't make sense. For this
reason, there are a bunch of problems where this needs consideration.

There are many applications that need to identify this:

  - average measurements together
  - interpolation between measurements

# Enumerating Average Types

Let the term "average type" mean a method for combining two datums, with
weights that measure the relevance of each point. Then:

1.  linear averaging (a1,w1,a2,w2) -\> ( a1\*w1 + a2\*w1 ) / ( w1+w2 )
2.  geometric averaging (a1,w1,a2,w2) -\> ( a1\*w1 \* a2\*w1 ) / (
    w1\*w2 )
3.  nearest neighbor averaging (a1,w1,a2,w2) -\> (w1\>w2) ? a1 : a2
4.  if equal averaging (a1,w1,a2,w2) -\> ( a1==a2 ) ? a1 : FILL
5.  no averaging (a1,w1,a2,w2) -\> FILL
6.  max averaging (a1,w1,a2,w2) -\> a1\>a2 ? a1 : a2

## CDAWeb ISTP AVG\_TYPE

The CDF metadata "AVG\_TYPE" identifies additional modes:

1.  log (alias for geometric) logarithm of the average of the
    anti-logarithms of the values.
2.  RMS -- square root of the average of the squares of the values.
3.  decibel -- 10 times the logarithm of the average of the
    anti-logarithms of the (values/10.).
4.  cosine -- cosine of the average of the arc-cosines of the values.
5.  angle\_degrees -- "direction" average over 360 deg e.g., average of
    5 and 355 is 0 instead of 180.
6.  angle\_radians -- "direction" average over 2 pi
7.  angle\_hour -- "direction" average over local times (hours), e.g.,
    average of 2 and 22 is 0 instead of 12.

## mod averaging

Suppose you want to find the average longitude, measured in degrees.
Here you need to consider that 359 and 1 are just 2 degrees apart:

1.  mod360 averaging (a1,w1,a2,w2) -\> ( a2-a1\>180 ? ( (a2-360)\*w1 +
    a1\*w2 ) / ( w1 + w2 ) ) (etc)

CDAWeb identifies these as angle\_hour, angle\_radians, and
angle\_degrees.


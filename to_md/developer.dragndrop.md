Purpose: I've been playing with the ability to drop URIs onto the
canvas, and I better document this feature.

Audience: users

# Introduction

We make a simple way to build up applications by allowing users to drop
data URIs onto the canvas.

# Drop Targets

If a URI is dropped onto a plot, then it's first PlotElement is reset to
plot the URI. If it is incomplete and rejected, then the data set editor
is entered.

If the URI is dropped just below or just above, then we insert a plot.

![dragndrop0.png](dragndrop0.png "dragndrop0.png")
![dragndrop1.png](dragndrop1.png "dragndrop1.png")

Audience: Science teams wanting more flexibility in their vaps.

# Introduction
When a .vap is loaded, it can contain "macros" which are template strings which are resolved 
as the .vap is loaded.  For example, %{PWD} is replaced with the directory (or web location) 
containing the .vap file.  

At some point a feature was added where arbitrary strings could be used.  So for example, you 
can have an annotation with the text "%{TODAY} %{MACHINE}" and then if the .vap is loaded
with https://autoplot.org/vap/macro.vap?TODAY=2025-06-05&MACHINE=draylax these values will
be substituted into the string.  Try loading 
https://github.com/autoplot/dev/blob/master/rfe/2026/20260227/demoTweakVap.vap?TODAY=2026-02-27
as another example.

There's a problem here with the design, where some words are reserved (%{PWD}, %{CONTEXT}, 
%{TIMERANGE}) and used by Autoplot, and others are used by the science team.  For this reason,
macros should be fairly unique and not likely to conflict.  See https://github.com/autoplot/documentation/wiki/Annotations .

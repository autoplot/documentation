Introduction. Right now, the title is derived from the metadata via a
metadata model. The CDF file reader says, this is ISTP compliant
metadata so CATDESC is the title. It might be nice to have the
flexibility for allowing the client to specify how this is done. This
might also finally deal with the problem of reporting the slice location
as well, which current uses "\!c(.\*)=(.\*)" to find the text to replace
on updates.

title=%{CATDESC}

title=%{USER\_PROPERTIES.CATDESC} @ %{CONTEXT}

yaxis label=%{LABEL}(%{UNITS})

Note USER\_PROPERTIES are properties QDataSet propogates but doesn't
interpret.

Note the Axis tab titles and labels have a right-click context menu to
add macros.

# Current Support

See
<sftp://papco.org/home/jbf/ct/autoplot/script/development/rfe426/demo.jyds>

## Legend Label

%{USER\_PROPERTIES.VERSION} works. I had to add a putProperty branch
that would support PyDict to use this in a Jython script.

Get data from CDF metadata: Mission Group:
%{METADATA.GlobalAttributes.Mission\_group}\!cSource:
%{METADATA.GlobalAttributes.Source\_name}

## Title

%{USER\_PROPERTIES.VERSION} does not work.

I've made it so that the title and the plotElement legend use the same
code. This code assumes that it's okay to use the first plot element to
get dataset metadata.

## XAxis and YAxis


1.  QFunction

<!-- end list -->

1.  1.  From autoplot.org

Jump to: \[navigation\](\#column-one), \[search\](\#searchInput)

Definitive Page On QFunctions

A QFunction is a representation for a data function that tries to reuse
as much of the QDataSet interface as possible. A QFunction takes N
parameters as input and returns M parameters as output. The QFunction
interface is simply a value() method that takes a rank 1 dataset as
input and returns a rank 1 dataset as output. Also a method
exampleInput() returns an example of an input used for the function.
This allows for discovery of the function, identifying units, valid
ranges, and cadences for inputs.

\`\`\`

```
interface QFunction {
  QDataSet value( QDataSet in );   // rank 1 input of N parameters and rank 1 output of M values.
  QDataSet exampleInput();
}
```
\`\`\`

\`\`\`

```
class DemoFunction implements QFunction {
  public QDataSet value( QDataSet in ) {
      return Ops.sin( in );
  }
  public QDataSet exampleInput() {
      MutablePropertyDataSet bds= new DDataSet(2,1);
      bds.putProperty( 0, QDataSet.UNITS, Units.dimensionless );
      bds.putProperty( 0, QDataSet.TYPICAL_MIN, -Math.PI );
      bds.putProperty( 0, QDataSet.TYPICAL_MAX, Math.PI );
      DDataSet v= DDataSet.wrap( 0. );
      v.putProperty( QDataSet.BUNDLE_0, bds );        
      return v;
}
```
\`\`\`

This is slightly extended to simply implementations and allow for more
efficient use when multiple invocations will be made:

\`\`\`

```
interface QFunction {
  QDataSet value( QDataSet in );   //
  QDataSet values( QDataSet in );  // rank 2 input and rank 2 output.
  QDataSet exampleInput();         // 
  QDataSet exampleOutput();        // call this when you just need the output.
}
```
\`\`\`

Note that implementations of a QFunction may simply check the the
BUNDLE\\\_0 pointer has not changed to know that none of the properties
have changed.

Here is how QDataSet properties are interpreted in this case:

\`\`\`

```
   * discover an example input.  Result is a rank 1 bundle QDataSet.
   *   QFunction ff= TestFunction();
   *   ff.exampleInput().length();  // how many parameters the function takes
   *   QDataSet bds= ff.exampleInput().property( QDataSet.BUNDLE_0 );  // get the bundle descriptor
   *   ; to discover properties of the first (0th) parameter:
   *   bds.slice(0).property( QDataSet.UNITS )       // function should handle convertible units (e.g. TimeAxes Ephemeris).
   *   bds.slice(0).property( QDataSet.VALID_MIN )   // absolute limits of domain of the function
   *   bds.slice(0).property( QDataSet.VALID_MAX )
   *   bds.slice(0).property( QDataSet.TYPICAL_MIN ) // domain of the function parameter
   *   bds.slice(0).property( QDataSet.TYPICAL_MAX )
   *   bds.slice(0).property( QDataSet.CADENCE ) // granularity of the function parameter
   *   bds.slice(0).property( QDataSet.LABEL )   // label for the parameter
   * slice(0) is the first argument, slice(1) would be the second, etc.
   * This would be a bundle.
```
\`\`\`

1.  Rank handling

QFunctions have two methods: value() and values(). \`value\` always
takes a rank 1 bundle. Even if this is just one parameter, then this
must be a bundle of the one parameter. \`values\` is always a rank 2.
The class AbstractQFunction is intended to simply writing QFunctions by
implementing a values method that calls the value method for each input
of the rank 2 array. This allows the QFunctions to be implemented more
efficiently when a lookup must be done before a result can be formed.
For example, at the Plasma Wave group, we implement functions by posting
the input to a server and then returning the result.

Retrieved from

```
   "<http://autoplot.org//QFunction>"
```
1.  1.  Views

```
 - [Article](/QFunction "View the content page [c]")

 - [Discussion](/wiki/index.php?title=Talk:QFunction&action=edit "Discussion about the content page [t]")

 - [View
   source](/wiki/index.php?title=QFunction&action=edit "This page is protected. You can view its source. [e]")

 - [History](/wiki/index.php?title=QFunction&action=history "Past versions of this page. [h]")
```
1.  1.  Personal tools

```
 - [Log in / create
   account](/wiki/index.php?title=Special:Userlogin&returnto=QFunction "You are encouraged to log in, it is not mandatory however. [o]")
```
\[\](/Main\_Page "Visit the Main Page \[z\]")

1.  1.  Navigation

```
 - [Main Page](/Main_Page "Visit the Main Page [z]")

 - [Community
   portal](/autoplot.org:Community_Portal "About the project, what you can do, where to find things")

 - [Current
   events](/Current_events "Find background information on current events")

 - [Recent
   changes](/Special:Recentchanges "The list of recent changes in the wiki. [r]")

 - [Random page](/Special:Random "Load a random page [x]")

 - [Help](/Help:Contents "The place to find out.")

 - [Donations](/autoplot.org:Site_support "Support us")
```
1.  1.  Search

&nbsp;

1.  1.  Toolbox

```
 - [What links
   here](/Special:Whatlinkshere/QFunction "List of all wiki pages that link here [j]")

 - [Related
   changes](/Special:Recentchangeslinked/QFunction "Recent changes in pages linked from this page [k]")

 - [Upload file](/Special:Upload "Upload images or media files [u]")

 - [Special
   pages](/Special:Specialpages "List of all special pages [q]")

 - [Printable
   version](/wiki/index.php?title=QFunction&printable=yes "Printable version of this page [p]")

 - [Permanent
   link](/wiki/index.php?title=QFunction&oldid=2682 "Permanent link to this version of the page")
```
\[\!\[Powered by
MediaWiki\](/wiki/skins/common/images/poweredby\_mediawiki\_88x31.png)\](http://www.mediawiki.org/)


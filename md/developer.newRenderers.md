Purpose: Describe how new Renderers are added to Das2.

Audience: Das2 developers and people interested in extending das2.

See also: <http://autoplot.org//developer.renderTypes> which outlines
existing renderer types.

# Introduction

Renderers convert data into pixels for the user.

**Note: This has changed, see the renderer keyword of the plot command**

# Renderer interface

Renderer is an interface for which just one method needs to be
implemented, render. In the render method, a Java2D graphics context is
provided, as well as the x and y axes. A monitor object is provided as
well, but it is typically not used.

The two axes passed in are used to convert data to a horizontal and
vertical coordinates.

```
   public void render(Graphics g, DasAxis xAxis, DasAxis yAxis, ProgressMonitor mon) {
       QDataSet bds= (QDataSet) ds.property(QDataSet.BUNDLE_1);
       Units xunits= (Units) bds.property(QDataSet.UNITS,0);
       Units yunits= (Units) bds.property(QDataSet.UNITS,1);
       for ( int i=0; i<ds.length(); i++ ) {
           QDataSet ds1= ds.slice(i);
           int ix= (int)xAxis.transform( ds1.value(0), xunits );
           int iy= (int)yAxis.transform( ds1.value(1), yunits );
           int radius= (int)( 1.0 * ( xAxis.transform( ds1.value(0) + ds1.value(2), xunits ) - ix ) ); 
           int irgb= (int)ds1.value(3);
           g.setColor( new Color(irgb) );
           g.fillOval( ix-radius, iy-radius, radius*2, radius*2 );
       }
   }
```

Rarely do renderers stay this small long, and a fully-developed code is
here:
<https://saturn.physics.uiowa.edu/svn/das2/dasCore/community/autoplot2011/trunk/dasCore/src/test/graph/MyRenderer.java>
. This adds a property "scale" and supports the control property which
is a string property containing the entire state in one string.
<https://saturn.physics.uiowa.edu/svn/das2/dasCore/community/autoplot2011/trunk/dasCore/src/test/graph/DemoAddRender.java>
shows the renderer in use.

# Spectrograms

Note spectrograms need a colorbar as well. This is a property of the
SpectrogramRenderer, which uses the Colorbar to look up color for the
value.

# PitchAngleDistributionRenderer

Just as soon as an interface is designed, it is bent and warped to work
in other use cases. This has happened with the
PitchAngleDistributionRenderer, which warps data which is polar into a
cartesian space.

# Implementing in Jython

Autoplot allows Jython to specify new Renderers. For example:

```
reset()
from org.das2.graph import Renderer
from org.das2.datum import EnumerationUnits
class MyRenderer( Renderer ):
  def render( self, g, xaxis, yaxis, monitor ):
    ds= self.getDataSet();
    for ds1 in ds:
       msg= ds1.slice(2).toString(); 
       g.drawString( msg, xaxis.transform( datum( ds1.slice(0) ) ), yaxis.transform( datum( ds1.slice(1) ) ) )    
rend= MyRenderer()
```
  
```
dsb= DataSetBuilder( 2, 100, 3 )
dsb.setUnits( 0, Units.us2000 )
dsb.setUnits( 1, Units.dimensionless )
dsb.setUnits( 2, EnumerationUnits( 'SCEvent' ) )
dsb.putValue( -1, 0, '2003-05-10 05:00' )
dsb.putValue( -1, 1, 124.0 )
dsb.putValue( -1, 2, 'on')
dsb.nextRecord()
rend.setDataSet( dsb.getDataSet() )
dom.plots[0].controller.dasPlot.addRenderer( rend )
bind(  dom, 'timeRange', dom.plots[0].xaxis, 'range' )
dom.timeRange= datumRange( '2003-05' )
dom.plots[0].yaxis.range= datumRange('0 to 140')
```

This script, when run, adds a new renderer.


# Introduction

Often in our field we need to survey long data sets, looking through images one at a time for interesting 
features. Autoplot's PNG Walk Tool facility will generate fixed images for intervals covering time range, 
or a "PNG Walk." For example, you have a useful product (vap file) that shows a day of data from a four year 
mission. You can then tell Autoplot to create daily plots for each day of the mission, producing roughly 
4 * 365 images. Autoplot's PNG Walk Viewer is a tool which allows you to then look at this PNG walk, where 
you can flip through the images quickly. Several different layouts of the thumbnails are provided, and you 
can click on the "View in Autoplot" button to reload Autoplot with the configuration used to make the image.

The PNG Walk Viewer is designed to work with any folder filled with images, from other groups' image walks, 
to test output and vacation pictures. The files need not be pngs either, .gif and .jpg files will work as 
well. To look at another group's walk, point the PNG Walk Viewer to either a templated file location like 
http://autoplot.org/data/pngwalk/product_$Y$m$d.png or simply a wildcard like 
http://autoplot.org/data/pngwalk/product_*.png. The PNG Walk Viewer will look for Autoplot features, like 
a folder called "thumbs400" where thumbnails can be loaded quickly.


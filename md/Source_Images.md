# Images

This data source reads images using Java's ImageIO library. The images
are mapped to a QDataSet internally.

  - mime type:
  - extension: .gif .jpg .png

  - Example URL
    [19](https://autoplot.org/data/image/Capture_00158.jpg?channel=greyscale)

  - Parameters
      - **channel** specifies how components should be combined to
        produce the rank 2 dataset.
          - If channel is not specified, then a rank 3 dataset with
            original image channels results.
          - Example channels include:
          - red, green, blue
          - hue, saturation, value (brightness)
          - greyscale is faster to calculate than value
      - **plotInfo=0** grab the axis information from the richPng
        metadata. See <https://autoplot.org/richPng>. (Note log=1 doesn't
        work with 24-bit color images.)
      - **xaxis=\[valmin,pixmin,valmax,pixmax\]** apply the axis
        transform on the horizontal axis.
      - **yaxis=\[valmin,pixmin,valmax,pixmax\]** apply the axis
        transform on the vertical axis.
      - **fog=90** apply 90% opaque fog to the image before displaying.
      - **blur=5** apply a 5=pixel wide blur kernal
      - **rotate=0** rotate the image clockwise degrees.

Note images can be loaded onto the canvas using annotations as well.  This
is how branding and provisional labels should be added to plots.
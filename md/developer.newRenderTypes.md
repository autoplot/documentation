Adding a new data renderer (spectrogram, line, digital, etc) is
possible, and should some day be as easy as adding data sources. Right
now you need to:

1.  define the das2 renderer in das2.
2.  search for DigitalRenderer
3.  Everywhere you find it, add analogous code for new type.
4.  RenderTypeUtil.needsColorbar


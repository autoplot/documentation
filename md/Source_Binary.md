BinaryTableReader reads in datasets from binary files. Data are assumed
to be in records of fixed-length.

  - extension: .bin
  - URI prefix: vap+bin
  - example URI:
    vap+bin:<file:///media/mini/data.backup/examples/bin/fromidl.bin?type=float&fieldCount=2&column=1>
  - supports formatting: yes, rank 1 and 2, written out as doubles.
  - parameters
      - **byteOffset** int, number of bytes skip before reading the
        data. default is 0.
      - **byteLength** int, total number of bytes to read. default is
        the content length.
      - **recLength** int, the number of bytes per record.
      - **recOffset** int, the byte offset into the record.
      - **fieldCount** int, number of fields per record, when recLength
        is not specified. default is 1.
      - **column** int, field number for the dependent parameter, then
        recOffset is not specified.
      - **dims=\[48,64\]** int array, specify dimensions of rank 2 table
        within each record.
      - **rank2=:** string like ":" or "5:15" to specify the positions
        to read in as table.
      - **type** data type for the dependent parameter. double, float,
        long, int, short, byte, ubyte. Default is ubyte.
      - **depend0Offset** int, byte offset into each record for the
        independent parameter.
      - **depend0** int, field number for the independent parameter when
        depend0Offset is not specified. Default is no independent
        parameter and the byte offset is the independent parameter.
      - **depend0Type** data type for the independent parameter. double,
        float, long, int, short, byte.
      - **byteOrder** data type byte order (endianness). little or big.
        Default is little.
      - **validMin**, double minimum valid value
      - **validMax**, double, maximum valid value
      - **recFormat**, string, format specifier for each record.
          - "d,13f" 8-byte double followed by 13 (4-byte) floats
          - "i,s,ub" int, short, unsigned byte
          - "x,ub,ui" skip byte, unsigned byte, unsigned int

#### Use-cases

**Reverse engineer binary format** How to reverse engineer a binary file
with the binary reader:

  - Plot the data using the default 1-byte data.
  - Look for the courser repeating pattern, which are probably records.
    Timetags will typically identify records, because they are far from
    zero. Set recLength= this length. rank2 can be used to look at each
    records bytes in a spectrogram.
  - Look for a repeating pattern. This implies a data type. For example,
    if every fourth point is a peak, then try type=float. If the period
    is 15 bytes long, then try to identify the data type of the first
    field by using recLength=15\&type=float, recLength=15\&type=double,
    etc. Once the first field's data type is appearent, it's easy to see
    if the recLength is correct. Use recOffset to look at other bytes
    within each record.
  - If you're getting repeating data with large exponents, then try
    byteOrder=big
  - Once the byteOrder is determined, then it's much easier to identify
    fields.
  - Example where the query parameters were figured out by the above
    approach:
    [3](vap+bin:https://space.physics.uiowa.edu/plasma-wave/voyager/data/pra/v1790205?reportOffset=yes&rank2=6:262&recLength=528&type=ushort&byteOrder=big)

**UTF16 to ASCII** Netbeans writes out a Unicode file of its output
window using 16-bit unicode. (I could tell this because ascii values were interleaved with
zeros.) `iconv` failed to convert the file, so I tried converting it
with Autoplot:

```
ds= getDataSet('vap+bin:file:///tmp/output1249405460816')
# skip every other record, skipping the zeroth record.
ds2= ds[1::2]  
# save it out as a binary stream.
formatDataSet( ds2, 'vap+bin:file:///tmp/output1249405460816.txt?type=ubyte' )
```

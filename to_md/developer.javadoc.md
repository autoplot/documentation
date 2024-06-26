Purpose: Define standards for Javadoc coding. Note I believe another
similar document exists, but I couldn't find it.

Audience: Developers and Javadoc consumers.

See also:
<https://ci-pw.physics.uiowa.edu/job/autoplot-javadoc/lastSuccessfulBuild/artifact/doc/index-all.html>

# Introduction

There need to be standards for coding Java docs. These include the
third-person voice and other standards you find described in books and
on the web, but also issues with documenting Autoplot and QDataSets.
Further the public Javadoc documentation is lacking, and this should
serve as a place for notes.

# Argument Position

QDataSets have properties like DEPEND\_0 that refer to the 0th index,
but often in documentation this is called the first index.

# Bean Properties

Bean properties should have four items:

  - a setter for writing to the property.
  - a getter for reading the property.
  - the member variable used to implement the property.
  - a string constant used as a handle for the property and to tag
    property events.

So how should each be documented? I think a reasonable standard is:

  - the getter and setting should document use for the client of the
    code. The getter and setter should use as much the same wording as
    possible. The setter should describe any side-effects to the client.
  - the member variable should contain any special notes about the
    implementation.
  - the handle should be standard not prompting any additional thought
    by the client or the author. It is only a handle so use of the
    property is possible.

Note this is tedious, but need only be done once. It's utility is
limited, but it asserts maturity of the code.

`   /**`  
`    * the line thickness in pixels.`  
`    */`  
`   private double lineThick = 1.0;`  
  
`   /**`  
`    * handle for the property lineThick.`  
`    */`  
`   public static final String PROP_LINETHICK = "lineThick";`  
  
`   /**`  
`    * get the line thickness in pixels.`  
`    * @return the line thickness in pixels.`  
`    */`  
`   public double getLineThick() {`  
`   }`  
  
`   /**`  
`    * set the line thickness in pixels.`  
`    * @param newlineThick the line thickness in pixels.`  
`    */`  
`   public void setLineThick(double newlineThick) {`  
`   }`

This seems awfully redundant, but JavaBeans are redundant, and when
things aren't consistent, you get strange behavior.

# code examples

There's a javadoc convention for including code blocks.

# references to other codes

The javadoc @see should be used with either:

`@see #guessBackingStore(org.das2.qds.QDataSet) `

or

`@see #copy(org.das2.qds.QDataSet) copy`

where "copy" is the label which describes the goal of the link, or

`@see #copy(org.das2.qds.QDataSet) copy, which copies the data.`

``` xml
<?xml version="1.0" encoding="UTF-8" ?>
<autoplot-bookmark-list xmlns="http://autoplot.org/schema/bookmarks"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
    <bookmark-folder>
        <title>Folder 1</title>
        <description>Folder 1 description</description>
        <bookmark-list>
            <bookmark>
                <title>Bookmark 1 title</title>
                <description>Bookmark 1 description</description>
                <url>http://autoplot.org/data/autoplot.cdf</url>
            </bookmark>
        </bookmark-list>
    </bookmark-folder>
    <bookmark-folder>
        <title>Folder 2</title>
        <description>Folder 2 description</description>
        <bookmark-list>
            <bookmark>
                <title>Bookmark 1 title</title>
                <description>Bookmark 1 description</description>
                <url>http://autoplot.org/data/autoplot.cdf</url>
            </bookmark>
        </bookmark-list>
    </bookmark-folder>
    <bookmark-folder remoteUrl="http://autoplot.org/data/CDAWeb.xml">
        <title>CDAWeb</title>
        <description>CDAWeb bookmarks</description>
    </bookmark-folder>
</autoplot-bookmark-list>
```
`
```

``` xml
<schema xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://autoplot.org/schema/bookmarks"
    xmlns:tns="http://autoplot.org/schema/bookmarks" elementFormDefault="qualified">


    <element name="bookmark-list">
        <complexType>
            <sequence>

                <element name="bookmark">
                    <complexType>
                        <sequence>
                            <element name="title" type="string" minOccurs="1"
                                maxOccurs="1" />
                            <element name="description" type="string" minOccurs="0"
                                maxOccurs="1" />
                            <element name="url" type="string" minOccurs="1"
                                maxOccurs="1" />
                        </sequence>
                    </complexType>
                </element>


            </sequence>
        </complexType>
    </element>

    <element name="autoplot-bookmark-list">
        <complexType>
            <sequence>

                <element name="bookmark-folder">
                    <complexType>
                        <sequence>
                            <element name="title" minOccurs="1" maxOccurs="1" />
                            <element name="description" minOccurs="0" maxOccurs="1" />
                            <element ref="bookmark-list" />
                        </sequence>

                        <attribute name="remoteUrl" type="string" />

                    </complexType>
                </element>
            </sequence>
        </complexType>
    </element>

</schema>
```
`
```


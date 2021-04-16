# org.das2.dataset.AbstractVectorDataSetAbstract implementation of the VectorDataSet interface provided to make
 implementation of concrete base classes easier.  Subclasses only need to
 implement:<ul>
 <li>{@link VectorDataSet#getDatum(int)}</li>
 <li>{@link VectorDataSet#getDouble(int, org.das2.datum.Units)}</li>
 <li>{@link VectorDataSet#getInt(int, org.das2.datum.Units)}</li>
 <li>{@link DataSet#getPlanarView(java.lang.String)}</li>
</ul>
***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>


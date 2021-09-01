# Apply Conditional Statement

![](../../.gitbook/assets/Apply_Conditional_Statement.png)

![](../../.gitbook/assets/Apply_Conditional_Statement%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug_grasshopper/src//LB%20Apply%20Conditional%20Statement.py)

Convert a hourly Ladybug data collection to a continuous collection at a specific timestep.

This will be done either through linear interpolation or by culling out values that do not fit the timestep. It can also be used to convert a discontinous data collection to a continuous one by linearly interpolating over holes in the data set.

## Inputs

* **data \[Required\]**

  A list of aligned Data Collections to be evaluated against the \_statement. 

* **statement \[Required\]**

  A conditional statement as a string \(e.g. a &gt; 25\). 

  The variable of the first data collection should always be named 'a' \(without quotations\), the variable of the second list should be named 'b', and so on. 

  For example, if three data collections are connected to \_data and the following statement is applied: '18 &lt; a &lt; 26 and b &lt; 80 and c &gt; 2' The resulting collections will only include values where the first data collection is between 18 and 26, the second collection is less than 80 and the third collection is greater than 2. 

## Outputs

* **data**

  A list of Data Collections that have been filtered by the statement\_. 


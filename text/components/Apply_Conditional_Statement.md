# Apply Conditional Statement

![](../../images/components/Apply\_Conditional\_Statement.png)

![](../../images/icons/Apply\_Conditional\_Statement.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Apply%20Conditional%20Statement.py)

Convert a hourly Ladybug data collection to a continuous collection at a specific timestep.

This will be done either through linear interpolation or by culling out values that do not fit the timestep. It can also be used to convert a discontinous data collection to a continuous one by linearly interpolating over holes in the data set.

## Inputs

*   **data \[Required]**

    A list of aligned Data Collections to be evaluated against the \_statement.&#x20;
*   **statement \[Required]**

    A conditional statement as a string (e.g. a > 25).&#x20;

    The variable of the first data collection should always be named 'a' (without quotations), the variable of the second list should be named 'b', and so on.&#x20;

    For example, if three data collections are connected to \_data and the following statement is applied: '18 < a < 26 and b < 80 and c > 2' The resulting collections will only include values where the first data collection is between 18 and 26, the second collection is less than 80 and the third collection is greater than 2.&#x20;

## Outputs

*   **data**

    A list of Data Collections that have been filtered by the statement\_.&#x20;

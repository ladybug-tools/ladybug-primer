# Time Aggregate

![](../../images/components/Time\_Aggregate.png)

![](../../images/icons/Time\_Aggregate.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Time%20Aggregate.py)

Convert a DataCollection of point-in-time values to its time-aggregated equivalent.

For example, if the collection has a Power data type in W, this method will return a collection with an Energy data type in kWh.

## Inputs

*   **data \[Required]**

    A houry, sub-hourly or daily data collection that can be aggregated over time to yield data of a different metric. (eg. a data collection of Power values in W).&#x20;

## Outputs

*   **data\_aggr**

    The data collection aggregated over time. (eg. a data collection of Energy values in kWh).&#x20;

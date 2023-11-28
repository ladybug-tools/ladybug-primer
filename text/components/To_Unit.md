# To Unit

![](../../images/components/To\_Unit.png)

![](../../images/icons/To\_Unit.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20To%20Unit.py)

Convert a DataCollection to the input \_to\_unit.

## Inputs

*   **data \[Required]**

    A DataCollection to be converted to different units.&#x20;
*   **to\_unit**

    Text representing the unit to convert the DataCollection to (eg. m2). Connect the \_data and see the all\_unit output for a list of all currently-supported units for a given collection. The default won't perform any unit conversion on the output data.&#x20;

## Outputs

*   **all\_unit**

    A list of all possible units that the input \_data can be converted to.&#x20;
*   **data**

    The converted DataCollection.&#x20;

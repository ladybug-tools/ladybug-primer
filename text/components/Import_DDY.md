# Import DDY

![](../../images/components/Import\_DDY.png)

![](../../images/icons/Import\_DDY.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Import%20DDY.py)

Import data from a standard .ddy file.

## Inputs

*   **ddy\_file \[Required]**

    A .ddy file path on your system as a string.&#x20;

## Outputs

*   **location**

    A Ladybug Location object describing the location data in the DDY file.&#x20;
*   **design\_days**

    A list of DesignDay objects representing the design days contained within the ddy file.&#x20;

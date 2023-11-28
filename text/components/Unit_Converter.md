# Unit Converter

![](../../images/components/Unit\_Converter.png)

![](../../images/icons/Unit\_Converter.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Unit%20Converter.py)

Convert a value or list of values from one unit to another.

## Inputs

*   **values \[Required]**

    Values to be converted from one unit type to another.&#x20;
*   **from\_u \[Required]**

    Text indicating the units of the input \_values (eg. 'C')&#x20;
*   **to\_u \[Required]**

    Text indicating the units of the output values (eg. 'K')&#x20;

## Outputs

*   **all\_u**

    A text string indicating all possible units that can be plugged into \_from\_u and \_to\_u.&#x20;
*   **values**

    The converted numerical values.&#x20;

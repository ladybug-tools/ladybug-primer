# Unit Converter

![](../../.gitbook/assets/Unit_Converter.png)

![](../../.gitbook/assets/Unit_Converter%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug_grasshopper/src//LB%20Unit%20Converter.py)

Convert a value or list of values from one unit to another.

## Inputs

* **values \[Required\]**

  Values to be converted from one unit type to another. 

* **from\_u \[Required\]**

  Text indicating the units of the input \_values \(eg. 'C'\) 

* **to\_u \[Required\]**

  Text indicating the units of the output values \(eg. 'K'\) 

## Outputs

* **all\_u**

  A text string indicating all possible units that can be plugged into \_from\_u and \_to\_u. 

* **values**

  The converted numerical values. 


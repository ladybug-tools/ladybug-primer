## Area Normalize
![](../../images/icons/Area_Normalize.png) - [[source code]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug_grasshopper/src//LB%20Area%20Normalize.py)

![](../../images/components/Area_Normalize.png)

Get a Data Collection that is normalized by an area value. 

Note that this component will raise a ValueError if the data type in the header of the data collection is not normalizable to yeild a useful type. Also note that a ZeroDivisionError will be raised if the input area is equal to 0. 



#### Inputs
* ##### data [Required]
A Data Collection to be normalized by the input _area. 
* ##### area [Required]
Script variable Python 
* ##### unit 
Text for the units that the area value is in. Acceptable inputs include 'm2', 'ft2' and any other unit that is supported. (Default: m2). 

#### Outputs
* ##### data
A Ladybug data collection object derived from the operation between the two data inputs. 
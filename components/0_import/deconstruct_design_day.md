# Deconstruct Design Day

![](../../.gitbook/assets/Deconstruct_Design_Day.png)

![](../../.gitbook/assets/Deconstruct_Design_Day%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug_grasshopper/src//LB%20Deconstruct%20Design%20Day.py)

Deconstruct design day into parameters.

## Inputs

* **design\_day \[Required\]**

  A DesignDay object to deconstruct. 

## Outputs

* **name**

  The name of the DesignDay object. 

* **day\_type**

  Text indicating the type of design day \(ie. 'SummerDesignDay', 'WinterDesignDay' or other EnergyPlus days\). 

* **location**

  A Ladybug Location object describing the location of the design day. 

* **date**

  Date for the day of the year the design day 

* **dry\_bulb\_max**

  Maximum dry bulb temperature over the design day \(in C\). 

* **dry\_bulb\_range**

  Dry bulb range over the design day \(in C\). 

* **humidity\_type**

  Type of humidity to use. Will be one of the following:

  * Wetbulb
  * Dewpoint
  * HumidityRatio
  * Enthalpy

* **humidity\_value**

  The value of the humidity condition above. 

* **barometric\_p**

  Barometric pressure in Pa. 

* **wind\_speed**

  Wind speed over the design day in m/s. 

* **wind\_dir**

  Wind direction over the design day in degrees. 

* **sky\_type**

  Script output sky\_type. 

* **sky\_properties**

  A list of properties describing the sky above. For ASHRAEClearSky this is a single value for clearness. For ASHRAETau, this is the tau\_beam and tau\_diffuse. 


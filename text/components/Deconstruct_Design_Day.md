# Deconstruct Design Day

![](../../images/components/Deconstruct\_Design\_Day.png)

![](../../images/icons/Deconstruct\_Design\_Day.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Deconstruct%20Design%20Day.py)

Deconstruct design day into parameters.

## Inputs

*   **design\_day \[Required]**

    A DesignDay object to deconstruct.&#x20;

## Outputs

*   **name**

    The name of the DesignDay object.&#x20;
*   **day\_type**

    Text indicating the type of design day (ie. 'SummerDesignDay', 'WinterDesignDay' or other EnergyPlus days).&#x20;
*   **location**

    A Ladybug Location object describing the location of the design day.&#x20;
*   **date**

    Date for the day of the year the design day&#x20;
*   **dry\_bulb\_max**

    Maximum dry bulb temperature over the design day (in C).&#x20;
*   **dry\_bulb\_range**

    Dry bulb range over the design day (in C).&#x20;
*   **humidity\_type**

    Type of humidity to use. Will be one of the following:

    * Wetbulb
    * Dewpoint
    * HumidityRatio
    * Enthalpy
*   **humidity\_value**

    The value of the humidity condition above.&#x20;
*   **barometric\_p**

    Barometric pressure in Pa.&#x20;
*   **wind\_speed**

    Wind speed over the design day in m/s.&#x20;
*   **wind\_dir**

    Wind direction over the design day in degrees.&#x20;
*   **sky\_type**

    Script output sky\_type.&#x20;
*   **sky\_properties**

    A list of properties describing the sky above. For ASHRAEClearSky this is a single value for clearness. For ASHRAETau, this is the tau\_beam and tau\_diffuse.&#x20;

# Import Design Day

![](../../images/components/Import\_Design\_Day.png)

![](<../../images/icons/Import\_Design\_Day (1).png>) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Import%20Design%20Day.py)

Import hourly climate data from a Ladybug DesignDay object.

## Inputs

*   **design\_day \[Required]**

    A DesignDay object to import.&#x20;

## Outputs

*   **location**

    A Ladybug Location object describing the location of the design day.&#x20;
*   **dry\_bulb\_temperature**

    The houlry dry bulb temperature over the design day, in C.&#x20;
*   **dew\_point\_temperature**

    The hourly dew point temperature over the design day, in C.&#x20;
*   **relative\_humidity**

    The hourly Relative Humidity over the design day in percent.&#x20;
*   **wind\_speed**

    The hourly wind speed over the design day in m/sec.&#x20;
*   **wind\_direction**

    The hourly wind direction over the design day in degrees. The convention is that North=0.0, East=90.0, South=180.0, West=270.0.&#x20;
*   **direct\_normal\_rad**

    The hourly Direct Normal Radiation over the design day in Wh/m2.&#x20;
*   **diffuse\_horizontal\_rad**

    The hourly Diffuse Horizontal Radiation over the design day in Wh/m2.&#x20;
*   **global\_horizontal\_rad**

    The hourly Global Horizontal Radiation over the design day in Wh/m2.&#x20;
*   **horizontal\_infrared\_rad**

    The Horizontal Infrared Radiation Intensity over the design day in Wh/m2.&#x20;
*   **total\_sky\_cover**

    The fraction for total sky cover over the design day in tenths of coverage.&#x20;
*   **barometric\_pressure**

    The hourly weather station pressure over the design day in Pa.&#x20;

# Import STAT

![](../../images/components/Import\_STAT.png)

![](../../images/icons/Import\_STAT.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Import%20STAT.py)

Import data from a standard .stat file.

## Inputs

*   **stat\_file \[Required]**

    A .stat file path on your system as a string.&#x20;

## Outputs

*   **location**

    A Ladybug Location object describing the location data in the STAT file.&#x20;
*   **ashrae\_zone**

    The ASHRAE climate zone of the STAT file. Numbers in the zone denote average temperature (0 = Hottest; 8 = Coldest). Letters in the zone denote wetness (A = Humid; B = Dry; C = Marine)&#x20;
*   **koppen\_zone**

    The Koppen climate zone of the STAT file. The Koppen climate system uses vegetation as in indicator fo climate and combines average monthly temperatures, precipitation, and the seasonality of precipitation.&#x20;
*   **clear\_dir\_norm\_rad**

    The hourly "Clear Sky" Direct Normal Radiation in Wh/m2. Such clear sky radiation is typically used for sizing cooling systems. If monthly optical depths are found within the STAT file, these values will come from the Revised ASHARAE Clear Sky (Tau model). If no optical depths are found, they will come from the original ASHARE lear sky model.&#x20;
*   **clear\_diff\_horiz\_rad**

    The hourly "Clear Sky" Diffuse Horizontal Radiation in Wh/m2. Such clear sky radiation is typically used for sizing cooling systems. If monthly optical depths are found within the STAT file, these values will come from the Revised ASHARAE Clear Sky (Tau model). If no optical depths are found, they will come from the original ASHARE lear sky model.&#x20;
*   **ann\_heat\_dday\_996**

    A DesignDay object representing the annual 99.6% heating design day.&#x20;
*   **ann\_heat\_dday\_990**

    A DesignDay object representing the annual 99.0% heating design day.&#x20;
*   **ann\_cool\_dday\_004**

    A DesignDay object representing the annual 0.4% cooling design day.&#x20;
*   **ann\_cool\_dday\_010**

    A DesignDay object representing the annual 1.0% cooling design day.&#x20;
*   **monthly\_ddays\_050**

    A list of 12 DesignDay objects representing monthly 5.0% cooling design days.&#x20;
*   **monthly\_ddays\_100**

    A list of 12 DesignDay objects representing monthly 10.0% cooling design days.&#x20;
*   **extreme\_cold\_week**

    A Ladybug AnalysisPeriod object representing the coldest week within the corresponding EPW.&#x20;
*   **extreme\_hot\_week**

    A Ladybug AnalysisPeriod object representing the hottest week within the corresponding EPW.&#x20;
*   **typical\_weeks**

    A list of Ladybug AnalysisPeriod objects representing typical weeks within the corresponding EPW. The type of week can vary depending on the climate.&#x20;

    For mid and high lattitude climates with 4 seasons (eg. New York), these weeks are for each of the 4 seasons ordered as follows: Winter, Spring, Summer, Autumn&#x20;

    For low lattitude climates with wet/dry seasons (eg. Mumbai), these weeks might also include: Wet Season, Dry Season&#x20;

    For equitorial climates with no seasons (eg. Singapore), This output is usually a single week representing typical conditions of the entire year.&#x20;

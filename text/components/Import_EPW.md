# Import EPW

![](../../images/components/Import\_EPW.png)

![](../../images/icons/Import\_EPW.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Import%20EPW.py)

Import climate data from a standard .epw file.

## Inputs

*   **epw\_file \[Required]**

    An .epw file path on your system as a string.&#x20;

## Outputs

*   **location**

    A Ladybug Location object describing the location data in the weather file.&#x20;
*   **dry\_bulb\_temperature**

    The houlry dry bulb temperature, in C. Note that this is a full numeric field (i.e. 23.6) and not an integer representation with tenths. Valid values range from 70 C to 70 C. Missing value for this field is 99.9.&#x20;
*   **dew\_point\_temperature**

    The hourly dew point temperature, in C. Note that this is a full numeric field (i.e. 23.6) and not an integer representation with tenths. Valid values range from 70 C to 70 C. Missing value for this field is 99.9.&#x20;
*   **relative\_humidity**

    The hourly Relative Humidity in percent. Valid values range from 0% to 110%. Missing value for this field is 999.&#x20;
*   **wind\_speed**

    The hourly wind speed in m/sec. Values can range from 0 to 40. Missing value is 999.&#x20;
*   **wind\_direction**

    The hourly wind direction in degrees. The convention is North=0.0, East=90.0, South=180.0, West=270.0. If wind is calm for the given hour, the direction equals zero. Values can range from 0 to 360. Missing value is 999.&#x20;
*   **direct\_normal\_rad**

    The hourly Direct Normal Radiation in Wh/m2. Direc Normal Radiation is the amount of solar radiation in Wh/m2 received directly from the solar disk on a surface perpendicular to the sun's rays. Missing values are (9999).&#x20;
*   **diffuse\_horizontal\_rad**

    The hourly Diffuse Horizontal Radiation in Wh/m2. Diffuse Horizontal Radiation is the amount of solar radiation in Wh/m2 received from the sky (excluding the solar disk) on a horizontal surface. Missing values are (9999).&#x20;
*   **global\_horizontal\_rad**

    The hourly Global Horizontal Radiation in Wh/m2. Global Horizontal Radiation is the total amount of direct and diffuse solar radiation in Wh/m2 received on a horizontal surface. It is not currently used inbEnergyPlus calculations. It should have a minimum value of 0; missing value for this field is 9999.&#x20;
*   **horizontal\_infrared\_rad**

    The Horizontal Infrared Radiation Intensity in Wh/m2. If it is missing, EnergyPlus calculates it from the Opaque Sky Cover field. It should have a minimum value of 0; missing value is 9999.&#x20;
*   **direct\_normal\_ill**

    The hourly Direct Normal Illuminance in lux. Direct Normal Illuminance is the average amount of illuminance in lux received directly from the solar disk on a surface perpendicular to the sun's rays. It is not currently used in EnergyPlus calculations. It should have a minimum value of 0; missing value is 999999.&#x20;
*   **diffuse\_horizontal\_ill**

    The hourly Diffuse Horizontal Illuminance in lux. Diffuse Horizontal Illuminance is the average amount of illuminance in lux received from the sky (excluding the solar disk) on a horizontal surface. It is not currently used in EnergyPlus calculations. It should have a minimum value of 0; missing value is 999999.&#x20;
*   **global\_horizontal\_ill**

    The hourly Global Horizontal Illuminance in lux. Global Horizontal Illuminance is the average total amount of direct and diffuse illuminance in lux received on a horizontal surface. It is not currently used in EnergyPlus calculations. It should have a minimum value of 0; missing value is 999999.&#x20;
*   **total\_sky\_cover**

    The fraction for Total Sky Cover  in tenths of coverage. (eg. 1 is 1/10 covered. 10 is total coverage). Total Sky Cover is the amount of the sky dome covered by clouds or obscuring phenomena. Minium value is 0; maximum value is 10; missing value is 99.&#x20;
*   **barometric\_pressure**

    The hourly weather station pressure in Pa. Valid values range from 31,000 to 120,000. Missing value is 999999.&#x20;
*   **model\_year**

    The year from which the hourly data has been extracted. EPW files are synthesized from real recorded data from different years in a given climate. This is done to ensure that, for each month, the selected data is statistically representative of the average monthly conditions over the 18+ years of recording the data. Different EPW files will be synthesized from different years depeding on whether they are TMY (Typical Meteorological Year), TMY2, TMY3, AMY (Actual Meteorological Year) or other.&#x20;
*   **ground\_temperature**

    Monthly ground temperature data if it exists within the EPW file. Typically, each data collection in this list represents monthly temperatures at three different depths.

    * 0.5 meters
    * 2.0 meters
    * 4.0 meters

# Solar MRT from Solar Components

![](../../images/components/Solar\_MRT\_from\_Solar\_Components.png)

![](../../images/icons/Solar\_MRT\_from\_Solar\_Components.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Solar%20MRT%20from%20Solar%20Components.py)

Calculate Mean Radiant Temperature (MRT) as a result of shortwave solar using horizontal solar components (direct horizontal and diffuse horizontal solar).

This component uses the SolarCal model of ASHRAE-55 to estimate the effects of shortwave solar and a simple sky exposure method to determine longwave radiant exchange.

## Inputs

*   **location \[Required]**

    A Ladybug Location object.&#x20;
*   **longwave\_mrt \[Required]**

    A single number or an hourly data collection with the long-wave mean radiant temperature around the person in degrees C. This includes the temperature of the ground and any other surfaces between the person and their view to the sky. Typically, air temperature is used when such surface temperatures are unknown.&#x20;
*   **dir\_horiz\_rad \[Required]**

    Hourly Data Collection with the direct horizontal solar irradiance in W/m2.&#x20;
*   **diff\_horiz\_rad \[Required]**

    Hourly Data Collection with diffuse horizontal solar irradiance in W/m2.&#x20;
*   **fract\_body\_exp**

    A single number between 0 and 1 or a data collection representing the fraction of the body exposed to direct sunlight. Note that this does not include the body’s self-shading; only the shading from surroundings. Default is 1 for a person standing in an open area.&#x20;
*   **ground\_ref**

    A single number between 0 and 1 or a data collection that represents the reflectance of the floor. Default is for 0.25 which is characteristic of outdoor grass or dry bare soil.&#x20;
*   **solar\_body\_par**

    Optional solar body parameters from the "LB Solar Body Parameters" object to specify the properties of the human geometry assumed in the shortwave MRT calculation. The default assumes average skin/clothing absorptivity and a human subject always has their back to the sun at a 45-degree angle (SHARP = 135).&#x20;
*   **run \[Required]**

    Set to True to run the component.&#x20;

## Outputs

*   **report**

    Reports, errors, warnings, etc.&#x20;
*   **erf**

    Data collection of effective radiant field (ERF) in W/m2.&#x20;
*   **dmrt**

    Data collection of mean radiant temperature delta in C.&#x20;
*   **mrt**

    Data collection of mean radiant temperature in C.&#x20;

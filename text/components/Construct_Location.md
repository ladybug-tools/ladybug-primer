## ![](../../images/icons/Construct_Location.png) Construct Location

![](../../images/components/Construct_Location.png)

Construct location. -

#### Inputs
* ##### name [Default]
A name for the location you are constructing. (ie. Steventon Island, Antarctica)
* ##### latitude [Default]
The latitude of the location you are constructing. Values must be between -90 and 90. Default is set to the equator.
* ##### longitude [Default]
An optional numerical value representing the longitude of the location you are constructing. This can improve the accuracy of the resulting sun plot.
* ##### timeZone [Default]
An optional integer representing the time zone of the location you are constructing. This can improve the accuracy of the resulting sun plot.  The time zone should follow the epw convention and should be between -12 and +12, where 0 is at Greenwich, UK, positive values are to the East of Greenwich and negative values are to the West.
* ##### elevation [Default]
An optional numerical value representing the elevation of the location you are constructing.

#### Outputs
* ##### location
Location data (use this output to construct the sun path).


[Check Hydra Example Files for Construct Location](https://hydrashare.github.io/hydra/index.html?keywords=LadybugPlus_Construct Location)
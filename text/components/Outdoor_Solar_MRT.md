## ![](../../images/icons/Outdoor_Solar_MRT.png) Outdoor Solar MRT - [[source code]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug_grasshopper/src//LB%20Outdoor%20Solar%20MRT.py)

![](../../images/components/Outdoor_Solar_MRT.png)

Calculate Mean Radiant Temperature (MRT) as a result of outdoor shortwave solar shining directly onto people as well as longwave radiant exchange with the sky. 

This component uses the SolarCal model of ASHRAE-55 to estimate the effects of shortwave solar and a simple sky exposure method to determine longwave radiant exchange. 



#### Inputs
* ##### location [Required]
A Ladybug Location object, used to determine the altitude and azimuth of the sun. 
* ##### surface_temp [Required]
A single number or an hourly data collection with the temperature of surfaces around the person in degrees C. This includes the ground and any other surfaces blocking the view to the sky. Typically, outdoor dry bulb temperature is used when such surface temperatures are unknown. 
* ##### dir_norm_rad [Required]
Hourly Data Collection with the direct normal solar irradiance in W/m2. 
* ##### diff_horiz_rad [Required]
Hourly Data Collection with diffuse horizontal solar irradiance in W/m2. 
* ##### horiz_infrared [Required]
Hourly Data Collection with the horizontal infrared radiation intensity from the sky in W/m2. 
* ##### fract_body_exp 
A single number between 0 and 1 or a data collection for the fraction of the body exposed to direct sunlight. The "LB Human to Sky Relationship" component can be used to estimate this input for a given set of context geometry and position of the human. Note that this parameter does NOT include the body’s self-shading. It only includes the shading from furniture and surroundings. (Default: 1 for an open area). 
* ##### sky_exposure 
A single number between 0 and 1 or a data collection representing the fraction of the sky vault in the human subject’s view. The "LB Human to Sky Relationship" component can be used to estimate this input for a given set of context geometry and position of the human. (Default: 1 for a person standing in an open area). 
* ##### ground_ref 
A single number between 0 and 1 or a data collection that represents the reflectance of the floor. Default is for 0.25 which is characteristic of outdoor grass or dry bare soil. 
* ##### solar_body_par 
Optional solar body parameters from the "LB Solar Body Parameters" object to specify the properties of the human geometry assumed in the shortwave MRT calculation. The default assumes average skin/clothing absorptivity and a human subject always has their back to the sun at a 45-degree angle (SHARP = 135). 
* ##### run [Required]
Set to True to run the component. 

#### Outputs
* ##### report
Reports, errors, warnings, etc.
* ##### short_erf
Data collection of shortwave effective radiant field (ERF) in W/m2.
* ##### long_erf
Data collection of longwave effective radiant field (ERF) in W/m2.
* ##### short_dmrt
Data collection of shortwave mean radiant temperature delta in C.
* ##### long_dmrt
Data collection of longwave mean radiant temperature delta in C.
* ##### mrt
Data collection of mean radiant temperature in C.  This accounts for both the shortwave solar shining directly onto people as well as longwave radiant exchange with the sky.
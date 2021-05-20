## UTCI Comfort

![](../../images/components/UTCI_Comfort.png)

![](../../images/icons/UTCI_Comfort.png) - [[source code]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug_grasshopper/src//LB%20UTCI%20Comfort.py)


Calculate Universal Thermal Climate Index (UTCI). 

UTCI is a thermal comfort model strictly for the outdoors. It is an interational standard for outdoor temperature sensation (aka. "feels-like" temperature) and is the most common of such "feels-like" temperature metrics used by meteorologists. 

While UTCI is valid in all climates, seasons, and scales, it assumes that human subjects are walking and that they naturally adapt their clothing with the outdoor temperature. For outdoor situations that do not fit these criteria, the Physiological Equivalent Temperature (PET) model should be used. 



#### Inputs
* ##### air_temp [Required]
Data Collection or individual value of air temperature in C. 
* ##### mrt 
Data Collection or individual value of mean radiant temperature (MRT) in C. Default is the same as the air_temp. 
* ##### rel_humid [Required]
Data Collection or individual value of relative humidity in %. 
* ##### wind_vel 
Data Collection or individual of air speed values in m/s. Default is a low speed of 0.5 m/s, which is the lowest input speed that is recommended for the UTCI model. 
* ##### run [Required]
Set to True to run the component. 

#### Outputs
* ##### report
Reports, errors, warnings, etc. 
* ##### utci
Universal Thermal Climate Index (UTCI) in Celcius. 
* ##### comfort
Integers noting whether the input conditions result in no thermal stress. 
Values are one of the following: 

    * 0 = thermal stress

    * 1 = no thremal stress
* ##### condition
Integers noting the thermal status of a subject. 
Values are one of the following: 

    * -1 = cold

    *  0 = netural

    * +1 = hot
* ##### category
Integers noting the category that the UTCI conditions fall under on an 11-point scale. 
Values are one of the following: 

    * -5 = Extreme Cold Stress       (UTCI < -40)

    * -4 = Very Strong Cold Stress   (-40 <= UTCI < -27)

    * -3 = Strong Cold Stress        (-27 <= UTCI < -13)

    * -2 = Moderate Cold Stress      (-12 <= UTCI < 0)

    * -1 = Slight Cold Stress        (0 <= UTCI < 9)

    *  0 = No Thermal Stress         (9 <= UTCI < 26)

    * +1 = Slight Heat Stress        (26 <= UTCI < 28)

    * +2 = Moderate Heat Stress      (28 <= UTCI < 32)

    * +3 = Strong Heat Stress        (32 <= UTCI < 38)

    * +4 = Very Strong Heat Stress   (38 <= UTCI < 46)

    * +5 = Extreme Heat Stress       (46 < UTCI)
* ##### comf_obj
A Python object containing all inputs and results of the analysis.  This can be plugged into components like the "Comfort Statistics" component to get further information. 
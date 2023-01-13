## UTCI Comfort

![](../../images/components/UTCI_Comfort.png)

![](../../images/icons/UTCI_Comfort.png) - [[source code]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug_grasshopper/src//LB%20UTCI%20Comfort.py)


Calculate Universal Thermal Climate Index (UTCI). 

UTCI is a thermal comfort model strictly for the outdoors. It is an international standard for outdoor temperature sensation (aka. "feels-like" temperature) and is one of the most common of such "feels-like" temperatures used by meteorologists. UTCI that attempts to satisfy the following requirements: 

1) Thermo-physiological significance in the whole range of heat exchange conditions. 2) Valid in all climates, seasons, and scales. 3) Useful for key applications in human biometeorology. 

While UTCI is designed to be valid in all climates and seasons, it assumes that human subjects are walking (with a metabolic rate around 2.4 met) and that they naturally adapt their clothing with the outdoor temperature. For outdoor situations that do not fit these criteria, the Physiological Equivalent Temperature (PET) model is recommended. 



#### Inputs
* ##### air_temp [Required]
Data Collection or individual value for air temperature in C. 
* ##### mrt 
Data Collection or individual value for mean radiant temperature (MRT) in C. Default is the same as the air_temp. 
* ##### rel_humid [Required]
Data Collection or individual value for relative humidity in %. Note that percent values are between 0 and 100. 
* ##### wind_vel 
Data Collection or individual value for meteoroligical wind velocity at 10 m above ground level in m/s. Note that this meteorological velocity at 10 m is simply 1.5 times the speed felt at ground level in the original Fiala model used to create the UTCI model. Therefore, multiplying air speed values at the height of the human subject by 1.5 will make them a suitable input for this component. Default is a low speed of 0.5 m/s, which is the lowest input speed that is recommended for the UTCI model. 
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
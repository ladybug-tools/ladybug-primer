# Humidity Metrics

![](../../.gitbook/assets/Humidity_Metrics.png)

![](../../.gitbook/assets/Humidity_Metrics%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug_grasshopper/src//LB%20Humidity%20Metrics.py)

Calculate humidity metrics from relative humidity, dry bulb temperature and \(if present\) atmospheric pressure.

## Inputs

* **dry\_bulb \[Required\]**

  A value or data collection representing  dry bulb temperature \[C\] 

* **rel\_humid \[Required\]**

  A value or data collection representing relative humidity \[%\] 

* **pressure**

  A value or data collection representing atmospheric pressure \[Pa\] Default is to use air pressure at sea level \(101,325 Pa\). 

## Outputs

* **humid\_ratio**

  A data collection or value for humidity ratio \(aka. absolute humidity\). Units are fractional \(kg water / kg air\). 

* **enthalpy**

  A data collection or value for enthalpy \(kJ / Kg\). 

* **wet\_bulb**

  A data collection or value for wet bulb temperature \(C\). 

* **dew\_point**

  A data collection or value for dew point temperature \(C\). 


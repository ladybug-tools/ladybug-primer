# Humidity Metrics

![](../../images/components/Humidity\_Metrics.png)

![](../../images/icons/Humidity\_Metrics.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Humidity%20Metrics.py)

Calculate humidity metrics from relative humidity, dry bulb temperature and (if present) atmospheric pressure.

## Inputs

*   **dry\_bulb \[Required]**

    A value or data collection representing  dry bulb temperature \[C]&#x20;
*   **rel\_humid \[Required]**

    A value or data collection representing relative humidity \[%]&#x20;
*   **pressure**

    A value or data collection representing atmospheric pressure \[Pa] Default is to use air pressure at sea level (101,325 Pa).&#x20;

## Outputs

*   **humid\_ratio**

    A data collection or value for humidity ratio (aka. absolute humidity). Units are fractional (kg water / kg air).&#x20;
*   **enthalpy**

    A data collection or value for enthalpy (kJ / Kg).&#x20;
*   **wet\_bulb**

    A data collection or value for wet bulb temperature (C).&#x20;
*   **dew\_point**

    A data collection or value for dew point temperature (C).&#x20;

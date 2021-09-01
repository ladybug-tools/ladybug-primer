# Comfort Statistics

![](../../.gitbook/assets/Comfort_Statistics.png)

![](../../.gitbook/assets/Comfort_Statistics%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug_grasshopper/src//LB%20Comfort%20Statistics.py)

Get statitics of thermal comfort from a Ladybug Comfort Object.

## Inputs

* **comf\_obj \[Required\]**

  A Ladybug ComfortCollection object from any of the comfort model components. 

## Outputs

* **pct\_hot**

  The percent of time that conditions are hotter than acceptable limits. 

* **pct\_neutral**

  The percent of time that conditions are within acceptable limits \(aka. the percent of time comfortable\). 

* **pct\_cold**

  The percent of time that conditions are colder than acceptable limits. 


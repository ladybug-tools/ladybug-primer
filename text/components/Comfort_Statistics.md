# Comfort Statistics

![](../../images/components/Comfort\_Statistics.png)

![](../../images/icons/Comfort\_Statistics.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Comfort%20Statistics.py)

Get statitics of thermal comfort from a Ladybug Comfort Object.

## Inputs

*   **comf\_obj \[Required]**

    A Ladybug ComfortCollection object from any of the comfort model components.&#x20;

## Outputs

*   **pct\_hot**

    The percent of time that conditions are hotter than acceptable limits.&#x20;
*   **pct\_neutral**

    The percent of time that conditions are within acceptable limits (aka. the percent of time comfortable).&#x20;
*   **pct\_cold**

    The percent of time that conditions are colder than acceptable limits.&#x20;

# Construct Location

![](../../images/components/Construct\_Location.png)

![](../../images/icons/Construct\_Location.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Construct%20Location.py)

Construct location from latitude, lognitude, and time zone data.

## Inputs

*   **name**

    A name for the location you are constructing. For example, "Steventon Island, Antarctica". (Default: "-")&#x20;
*   **latitude**

    Location latitude between -90 and 90 (Default: 0).&#x20;
*   **longitude**

    Location longitude between -180 (west) and 180 (east) (Default: 0).&#x20;
*   **time\_zone**

    Time zone between -12 hours (west) and 12 hours (east). If None, the time zone will be an estimated integer value derived from the longitude in accordance with solar time (Default: None).&#x20;
*   **elevation**

    A number for elevation of the location in meters. (Default: 0).&#x20;

## Outputs

*   **location**

    Location data (use this output to construct the sun path).&#x20;

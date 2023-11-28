# Orient to Camera

![](../../images/components/Orient\_to\_Camera.png)

![](../../images/icons/Orient\_to\_Camera.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Orient%20to%20Camera.py)

Orient a series of geometries to the active viewport camera.

## Inputs

*   **geo \[Required]**

    A series of geometries to be oriented to the camera of the active Rhino viewport.&#x20;
*   **position**

    A point to be used as the origin around which the the geometry will be oriented. If None, the lower left corner of the bounding box around the geometry will be used.&#x20;
*   **refresh**

    Connect a Grasshopper "button" component to refresh the orientation upon hitting the button. You can also connect a Grasshopper "Timer" component to update the view in real time as you navigate through the Rhino scene.&#x20;

## Outputs

*   **geo**

    The input geometry that has been oriented to the camera of the active Rhino viewport.&#x20;

# Real Time Incident Radiation

![](../../images/components/Real\_Time\_Incident\_Radiation.png)

![](../../images/icons/Real\_Time\_Incident\_Radiation.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Real%20Time%20Incident%20Radiation.py)

Compute Incident Radiation values for any sky matrix in real time using the Geometry/Sky intersection matrix produced by the "LB Incident Radiation" component.

Using this component enables one to scroll through radiation on an hour-by-hour or month-by-month basis in a manner that is an order of magnitude faster than running each sky matrix through the "LB Incident Radiation" component.

The speed of this component is thanks to the fact that the Geometry/Sky intersection matrix contains the relationship between the geometry and each patch of the sky. So computing new radiation values is as simple as multiplying the sky matrix by the intersection matrix.

## Inputs

*   **int\_mtx \[Required]**

    A Geometry/Sky Intersection Matrix from the "LB Incident Radiation"  component. This matrix contains the relationship between each point of the analyzed geometry and each patch of the sky.&#x20;
*   **sky\_mtx \[Required]**

    A Sky Matrix from the "LB Cumulative Sky Matrix" component, which describes the radiation coming from the various patches of the sky. The "LB Sky Dome" component can be used to visualize any sky matrix.&#x20;

## Outputs

*   **results**

    A list of numbers that aligns with the points of the original analysis performed with the "LB Incident Radiation"  component. Each number indicates the cumulative incident radiation received by each of the points from the sky matrix in kWh/m2. To visualize these radiation values in the Rhino scene, connect these values to the "LB Spatial Heatmap" component along with the mesh output from the original analysis with the "LB Incident Radiation"  component.&#x20;

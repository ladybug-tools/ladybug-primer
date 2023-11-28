# Spatial Heatmap

![](../../images/components/Spatial\_Heatmap.png)

![](<../../images/icons/Spatial\_Heatmap (1).png>) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Spatial%20Heatmap.py)

Color a mesh as a heatmap using values that align with the mesh faces or vertices.

Note that any brep can be converted to a gridded mesh that can be consumed by this component using the "LB Generate Point Grid" component.

### Inputs

* **values \[Required]**

A list of numerical values with which to color the mesh. The number of values must match the number of faces or vertices in the mesh.

* **mesh \[Required]**

A Mesh object, with a number of faces or vertices that match the number of input values and will be colored with results.

* **offset\_dom**

Optional domain (or number for distance), which will be used to offset the mesh faces or verticesto according to the values. Higher values will be offset further.

* **legend\_par**

Optional legend parameters from the Ladybug 'Legend Parameters' component.

* **legend\_title**

A text string for Legend title. Typically, the units of the data are used here but the type of data might also be used. Default is an empty string.

* **global\_title**

A text string to label the entire mesh. It will be displayed in the lower left of the result mesh. Default is for no title.

### Outputs

* **mesh**

The input \_mesh that has been colored with results.

* **legend**

Geometry representing the legend for the mesh.

* **title**

A text object for the global\_title.

* **colors**

The colors associated with each input value.

* **legend\_par**

The input legend parameters with defaults filled for unset properties.

* **vis\_set**

Script variable Heatmap

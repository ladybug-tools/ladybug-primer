## Surface Ray Tracing

![](../../images/components/Surface_Ray_Tracing.png)

![](../../images/icons/Surface_Ray_Tracing.png) - [[source code]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug_grasshopper/src//LB%20Surface%20Ray%20Tracing.py)


Get a ray tracing visualization of direct sunlight rays reflected off of _source_geo and subsequently bouncing through a set of context_ geometries. 

Examples where this visualization could be useful include understading the reflection of light by a light shelf or testing to see whether a parabolic glass or metal building geometry might focus sunlight to dangerous levels at certain times of the year. 

Note that this component assumes that all sun light is reflected specularly (like a mirror) and, for more detailed raytracing analysis with diffuse scattering, the Honeybee Radiance components should be used. 



#### Inputs
* ##### vector [Required]
A sun vector (typically from the "LB SunPath" component), which will be used to evaluate the light boucing off of the _source_geo and through the context_. 
* ##### source_geo [Required]
A brep or mesh representing a surface off of which sun rays first bounce. Lists of breps or meshes are also acceptable. These surfaces will be used to generate the initial sun rays in a grid-like pattern. 
* ##### context 
Breps or meshes for conext geometry, which will reflect the sun rays after they bounce off of the _source_geo. 
* ##### grid_size [Required]
A positive number in Rhino model units for the average distance between sun ray points to generate along the _source_geo. 
* ##### bounce_count 
An positive integer for the number of ray bounces to trace the sun rays forward. (Default: 1). 
* ##### first_length 
A positive number in Rhino model units for the length of the sun ray before the first bounce. If unspecified, this will be the diagonal of the bounding box surrounding all input geometries. 
* ##### last_length 
A positive number in Rhino model units representing the length of the sun ray after the last bounce. If unspecified, this will be the diagonal of the bounding box surrounding all input geometries. 

#### Outputs
* ##### rays
A list of polylines representing the sun rays traced forward onto the _source_geo and then through the context_. 
* ##### int_pts
A data tree of intersection points one one branch for each of the rays above. 
## ![](../../images/icons/Direct_Sun_Hours.png) Direct Sun Hours - [[source code]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug_grasshopper/src//LB%20Direct%20Sun%20Hours.py)

![](../../images/components/Direct_Sun_Hours.png)

Calculate the number of hours of direct sunlight received by geometry using sun vectors obtained from the "LB SunPath" component. 

Such direct sun calculations can be used for shadow studies of outdoor enviroments or can be used to estimate glare potential from direct sun on the indoors. 

Note that this component uses the CAD environment's ray intersection methods, which can be fast for geometries with low complexity but does not scale well for complex geometries or many test points. For such complex studies, honeybee-radiance should be used. 



#### Inputs
* ##### vectors [Required]
Sun vectors from the "LB SunPath" component, which will be used to determine the number of hours of direct sunlight received by the test _geometry. 
* ##### timestep 
A positive integer for the number of timesteps per hour at which the "LB SunPath" component generated sun vectors. This is used to correctly interpret the time duration represented by each of the input sun vectors. (Default: 1 for 1 vector per hour). 
* ##### geometry [Required]
Rhino Breps and/or Rhino Meshes for which direct sun analysis will be conducted. If Breps are input, they will be subdivided using the _grid_size to yeild individual points at which analysis will occur. If a Mesh is input, direct sun analysis analysis will be performed for each face of this mesh instead of subdividing it. 
* ##### context 
Rhino Breps and/or Rhino Meshes representing context geometry that can block sunlight to the test _geometry. 
* ##### grid_size [Required]
A positive number in Rhino model units for the size of grid cells at which the input _geometry will be subdivided for direct sun analysis. The smaller the grid size, the higher the resolution of the analysis and the longer the calculation will take.  So it is recommended that one start with a large value here and decrease the value as needed. However, the grid size should usually be smaller than the dimensions of the smallest piece of the _geometry and context_ in order to yield meaningful results. 
* ##### offset_dist 
A number for the distance to move points from the surfaces of the input _geometry.  Typically, this should be a small positive number to ensure points are not blocked by the mesh. (Default: 10 cm in the equivalent Rhino Model units). 
* ##### legend_par 
Optional legend parameters from the "LB Legend Parameters" that will be used to customize the display of the results. 
* ##### parallel 
Set to "True" to run the study using multiple CPUs. This can dramatically decrease calculation time but can interfere with other computational processes that might be running on your machine. (Default: False). 
* ##### run [Required]
Set to "True" to run the component and perform direct sun analysis. 

#### Outputs
* ##### report
...
* ##### points
The grid of points on the test _geometry that are be used to perform the direct sun analysis.
* ##### results
A list of numbers that aligns with the points. Each number indicates the number of hours of direct sunlight received by each of the points.  Note that is is the number of hours out of the total number of connected _vectors.
* ##### mesh
A colored mesh of the test _geometry representing the hours of direct sunlight received by this input _geometry
* ##### legend
A legend showing the number of hours that correspond to the colors of the mesh.
* ##### title
A text object for the study title.
* ##### int_mtx
A Matrix object that can be connected to the "LB Deconstruct Matrix" component to obtain detailed vector-by-vector results of the study. Each sub-list of the matrix (aka. branch of the Data Tree) represents one of the points used for analysis. The length of each sub-list matches the number of _vectors used for the analysis. Each value in the sub-list is either a "1", indicating that the sun is visible for that vector, or a "0", indicating that the sun is not visible for that vector.
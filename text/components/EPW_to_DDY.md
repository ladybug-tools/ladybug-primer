## EPW to DDY

![](../../images/components/EPW_to_DDY.png)

![](../../images/icons/EPW_to_DDY.png) - [[source code]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug_grasshopper/src//LB%20EPW%20to%20DDY.py)


Produce a DDY file from the data contained within an EPW or STAT file. 

For EPW files, this method will first check if there is any heating or cooling design day information contained within the EPW itself. If None is found, the heating and cooling design days will be derived from analysis of the annual data within the EPW. This process of analyzing the annual TMY data is less representative of the climate since only one year of data is used to derive the DDY (instead of the usual multi-year analysis). However, if the EPW is the best available representation of the climate for a given site, it can often be preferable to using a DDY constructed with more years of data but from further away. Information on the uncertainty introduced by using only one year of data to create design days can be found in AHSRAE HOF 2013, Chapter 14.14. 

For STAT files, the DDY file will only be produced if the design day information is found within the file. If no information on the relevant design days are found, and error will be raised and the component will fail to run. 



#### Inputs
* ##### weather_file [Required]
The path to an .epw file or .stat file on your system, from which a .ddy will be generated. 
* ##### percentile 
A number between 0 and 50 for the percentile difference from the most extreme conditions within the EPW or STAT to be used for the design day. Typical values are 0.4 and 1.0. (Default: 0.4). 
* ##### monthly_cool 
A boolean to note whether the resulting .ddy file should contain twelve cooling design days for each of the months of the year. This type of DDY file is useful when the peak cooling might not be driven by warm outdoor temperatures but instead by the highest-intensity solar condition, which may not conincide with the highest temperature. Monthly conditions will be for the 2.0% hottest conditions in each month, which generally aligns with the annual 0.4% cooling design conditions. 
* ##### folder 
An optional file path to a directory into which the DDY file will be written.  If None, the DDY file will be written to the ladybug default weather data folder and placed in a sub-folder called "ddy". 
* ##### write [Required]
Set to "True" to write the .ddy file. 

#### Outputs
* ##### ddy_file
A .ddy file path that has been written to your system. 
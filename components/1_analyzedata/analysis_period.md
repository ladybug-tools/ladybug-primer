# Analysis Period

![](../../.gitbook/assets/Analysis_Period.png)

![](../../.gitbook/assets/Analysis_Period%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug_grasshopper/src//LB%20Analysis%20Period.py)

Create an Analysis Period to describe a slice of time during the year.

## Inputs

* **start\_month**

  Start month \(1-12\). 

* **start\_day**

  Start day \(1-31\). 

* **start\_hour**

  Start hour \(0-23\). 

* **end\_month**

  End month \(1-12\). 

* **end\_day**

  End day \(1-31\). 

* **end\_hour**

  End hour \(0-23\). 

* **timestep**

  An integer number for the number of time steps per hours. Acceptable inputs include: 1, 2, 3, 4, 5, 6, 10, 12, 15, 20, 30, 60 

## Outputs

* **period**

  Analysis period. 

* **hoys**

  List of dates in this analysis period. 

* **dates**

  List of hours of the year in this analysis period. 


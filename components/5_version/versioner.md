# Versioner

![](../../.gitbook/assets/Versioner.png)

![](../../.gitbook/assets/Versioner%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug_grasshopper/src//LB%20Versioner.py)

This component updates the Ladybug Tools core libraries and grasshopper components to either the latest development version available \(default\) or to a specific version of the grasshopper plugin.

The input version\_ does not need to be newer than the current installation and can be older but grasshopper plugin versions less than 0.3.0 are not supported. A list of all versions of the Grasshopper plugin and corresponding release notes can be found at: [https://github.com/ladybug-tools/lbt-grasshopper/releases](https://github.com/ladybug-tools/lbt-grasshopper/releases)

This component can also overwrite the user libraries of standards \(constructions, schedules, modifiers\) with a completely fresh copy if clean_standards_ is set to True.

## Inputs

* **update \[Required\]**

  Set to True to update your installation of Ladybug Tools to the latest development version or to be at the version specified below. 

* **version**

  An optional text string for the version of the grasshopper plugin which you would like to update to. The input should contain only integers separated by two periods \(eg. 1.0.0\). The version does not need to be newer than the current installation and can be older but grasshopper plugin versions less than 0.3.0 are not supported. A list of all versions of the Grasshopper plugin can be found here - [https://github.com/ladybug-tools/lbt-grasshopper/releases](https://github.com/ladybug-tools/lbt-grasshopper/releases) 

* **clean\_standards**

  Set to True to have the library of standards \(constructions, schedules, modifiers\) overwritten with a completely fresh copy. DO NOT SET TO TRUE IF YOU WANT TO KEEP ANY OBJECTS THAT YOU HAVE ADDED TO YOUR honeybee\_standards FOLDER. If False or None, any existing standards will be left alone. 

## Outputs

* **Vviiiiiz!**

  !!! 


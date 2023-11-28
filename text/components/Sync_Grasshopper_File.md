# Sync Grasshopper File

![](../../images/components/Sync\_Grasshopper\_File.png)

![](../../images/icons/Sync\_Grasshopper\_File.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Sync%20Grasshopper%20File.py)

Sync the Ladybug Tools components in a Grasshopper file with the version of the components that currently exist in the Grasshopper toolbar.

This is useful for updating old Grasshopper definitions to newer plugin versions. However, this component will sync components regardless of version number or date, even if the components in the toolbar are of an older version than those currently on the Grasshopper canvass.

Any components that cannot be updated automatically (because their inputs or outputs have changed) will be circled in red and should be replaced manually.

## Inputs

*   **sync \[Required]**

    Set to "True" to have this component to search through the current Grasshopper file and sync all Ladybug Tools components with the version in the Grasshopper toolbar.&#x20;

## Outputs

*   **report**

    Errors, warnings, etc.&#x20;

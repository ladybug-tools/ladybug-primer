# Mass Arithmetic Operation

![](../../images/components/Mass\_Arithmetic\_Operation.png)

![](../../images/icons/Mass\_Arithmetic\_Operation.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Mass%20Arithmetic%20Operation.py)

Perform a "mass" arithmetic operation between Data Collections. For example, adding a list of Data Collections into one Data Collection.

Note that Data Collections must be aligned in order for this component to run successfully.

Using this component will often be much faster and more elegant compared to deconstructing the data collection, performing the operation with native Grasshopper components, and rebuilding the collection.

## Inputs

*   **data \[Required]**

    A list of Data Collections to be used in the arithmetic operation.&#x20;
*   **operator**

    Text for the operator to use between the Data Collections. Valid examples include (+, -, \*, /). By default this is + for addition.&#x20;
*   **type**

    Optional text for a new "type" key in the Data Collection's metadata. This will usually show up in most Ladybug visualiztions and it should usually change for most types of operations.&#x20;

## Outputs

*   **data**

    A Ladybug data collection object derived from the operation between the two data inputs.&#x20;

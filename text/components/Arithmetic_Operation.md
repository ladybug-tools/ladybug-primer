# Arithmetic Operation

![](../../images/components/Arithmetic\_Operation.png)

![](../../images/icons/Arithmetic\_Operation.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Arithmetic%20Operation.py)

Perform simple arithmetic operations between Data Collections. For example, adding two Data Collections together, subtracting one collection from another, or multiplying/dividing a data in a collection by a factor.

Note that Data Collections must be aligned in order for this component to run successfully.

Using this component will often be much faster and more elegant compared to deconstructing the data collection, performing the operation with native Grasshopper components, and rebuilding the collection.

## Inputs

*   **data\_1 \[Required]**

    The first Data Collection in the operation. If the operator is not commutative, this collection comes before the operator. For example, in subtraction, this is the collection being subtracted from. This can also be a list of Data Collections that align with \_data\_2. It cal also be a single number that will be added, multiplied, etc. to all of \_data\_2.&#x20;
*   **data\_2 \[Required]**

    The second Data Collection in the operation. If the operator is not commutative, this collection comes after the operator. For example, in subtraction, this is the collection being subtracted with. This can also be a list of Data Collections that align with \_data\_1. It cal also be a single number that will be added, multiplied, etc. to all of \_data\_1.&#x20;
*   **operator**

    Text for the operator to use between the two Data Collections. Valid examples include (+, -, \*, /). By default this is + for addition.&#x20;
*   **type**

    Optional text for a new "type" key in the Data Collection's metadata. This will usually show up in most Ladybug visualiztions and it should usually change for most types of operations.&#x20;

## Outputs

*   **data**

    A Ladybug data collection object derived from the operation between the two data inputs.&#x20;

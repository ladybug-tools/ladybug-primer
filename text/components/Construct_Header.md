# Construct Header

![](../../images/components/Construct\_Header.png)

![](../../images/icons/Construct\_Header.png) - [\[source code\]](https://github.com/ladybug-tools/ladybug-grasshopper/blob/master/ladybug\_grasshopper/src/LB%20Construct%20Header.py)

Construct a Ladybug Header to be used to create a ladybug DataCollection.

## Inputs

*   **data\_type \[Required]**

    Text representing the type of data (e.g. Temperature). A full list of acceptable inputs can be seen by checking the all\_u output of the "LB Unit Converter" component. This input can also be a custom DataType object that has been created with the "LB Construct Data Type" component.&#x20;
*   **unit**

    Units of the data\_type (e.g. C). Default is to use the base unit of the connected\_data\_type.&#x20;
*   **a\_period**

    Script variable constrData&#x20;
*   **metadata**

    Optional metadata to be associated with the Header. The input should be a list of text strings with a property name and value for the property separated by a colon. For example:&#x20;

    .    source: TMY .    city: New York .    country: USA&#x20;

## Outputs

*   **header**

    A Ladybug Header object.&#x20;

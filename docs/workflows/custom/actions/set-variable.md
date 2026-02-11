# Action: Set variable

Responsible for declaring a local variable within the workflow. This is useful for storing a specific value that needs to be referenced in multiple locations, ensuring consistency and making the workflow easier to maintain.

## Input

| Variable          | Type   | Description                                                                          |
|-------------------|--------|--------------------------------------------------------------------------------------|
| **Variable name** | String | The unique name used to reference this value throughout the workflow.                |
| **Data type** | List   | The specific format of the data (see supported types below).                         |
| **Value** | Varied | The actual data or reference value to be stored in the variable.                     |

### Supported Data Types

Defining the correct type allows Workflow Builder to provide the appropriate interface (e.g., a search dialog or a toggle) when a user is prompted to provide a value.

* **String:** A simple scalar text value.
* **Number:** A numeric value (integer, floating point, etc.).
* **Boolean:** A true/false value.
* **Object:** A JSON data structure or associative array.
* **Array:** A list of multiple values.
* **Team ID:** A specific ID for a team chat or direct message conversation.

!!! info "Note on Referential Integrity"
    To maintain the stability of the workflow, you are not permitted to edit the data type of variables that are currently being referenced by other nodes in the workflow.

## Output

The node outputs individual variables as defined in the "Output variables" section.
# Action: comment

Inserts a log entry into the current workflow's history. This is especially helpful when trying to debug or troubleshoot a workflow, allowing users to see the value of a given variable to better understand how that variable may impact the logic or flow of a workflow. 

Comments have no functional impact on a workflow. 

## Input

| Variable            | Type   | Description                                     |
|---------------------|--------|-------------------------------------------------|
| **Comment text** | String | The message you wish to save to your workflow history. Users can insert variables into a comment that will be substituted for the corresponding value prior to the log entry being saved. To see a complete list of variables you can insert into a comment, type the "#" (hash sign) into the text input. |

## Output

None.

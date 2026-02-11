# Using variables in a workflow

## Types of variables

Variables are sometimes divided into different categories to facilitate selecting, finding and referencing the correct one within your workflow. These categories include:

### Trigger variables

These are the primary set of variables users will interact with. They refer to the variables that contain information that accompanied the event that triggered, or initiated the execution of the workflow. For triggers relating to SMS messages for example, this may include the phone number that sent the SMS, or received the SMS, or the SMS message itself. Each [trigger](./triggers/index.md) inserts its own set of variables into the current workflow's context. 

### Action output variables

These variables are not present when the workflow is first executed, but are instead added to the workflow as the result of executing an action. It can sometimes be helpful to think of these variables as an actions *output*. 

### User variables

These variables are present in every workflow and contain values associated with the user executing the workflow. This includes the user's name, phone number, and so forth. User variables include:

* My presence status
* My extension number
* My extension ID
* My account ID
* My first name
* My last name
* My email

## Usage

### Referencing variables

Variables can be referenced in any text field within Workflow Builder. They are ideal for use within the large text input boxes for an SMS message, or chat message. 

If you do not know the exact name of the variable you are looking for, type a "#" (pound-sign) into any text box and small help popup will appear to help you select the right one. 

### Setting variables

Variables are often created implicitly by a node. In some circumstances a workflow designer may wish to explicitly declare/create variable on their own. The following nodes enable this. 

<div class="grid cards actions" markdown>

- ![icon](../../img/icon-action-parse-json.png){ .icon-node } __[Parse JSON](actions/parse-json.md)__
- ![icon](../../img/icon-action-set-variable.png){ .icon-node } __[Set variable](actions/set-variable.md)__

</div>

<!--
### Liquid templating language

Workflow Builder uses the [Liquid templating language](https://shopify.github.io/liquid/) for referring to and manipulating variables. The Liquid language is a more advanced feature that gives users the ability to transform variable content, or conditionally display content according to your needs. 

#### Transforming text

Here are some examples of the kinds of things the Liquid language enables:

* [Date formatting](https://shopify.github.io/liquid/filters/date/)
* [Strip newlines](https://shopify.github.io/liquid/filters/strip_newlines/)
* [Find and replace strings](https://shopify.github.io/liquid/filters/replace/)
* [Force text to uppercase](https://shopify.github.io/liquid/filters/upcase/)
* See the [Liquid templating language](https://shopify.github.io/liquid/) for a full list
-->

<!--
#### Conditional logic using Liquid

One can also conditionally display text based on a variable's value, using simple if statements. For example:

```
{% if user.presenceStatus == "Busy" %}
  Sorry I couldn't take your call, but I am in focus mode right now. 
{% endif %}
```
-->


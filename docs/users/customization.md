# Converting templates to custom workflows

!!! warning "Converting a templated workflow to a custom workflow CANNOT be undone."
    Once a template has been converted to a custom workflow you will lose the ability to edit that workflow via a simple form. You will only be able to edit the workflow via the visual editor. 

Any workflow created from a template can be converted to a "custom workflow." [Custom workflows](../workflows/custom/index.md) are edited using a visual drag-and-drop design tool. They give users complete control over the workflow, allowing them to modify the logic of a workflow at a more fundamental level.

To customize a workflow created from a template, follow these steps:

1. Find the workflow in your list of workflows. 
2. Disable the workflow. 
3. From the more menu associated with that workflow, select "Convert to custom workflow."

<figure markdown>
  ![Converting a workflow to a custom workflow](../img/convert-to-advanced.png){ style="max-width: 400px" }
  <figcaption>Start with a template, and then customize it to meet your specific needs</figcaption>
</figure>

Upon completing the above steps you will be taken to the workflow designer for that workflow. 

While users do not need to know how to program in order to edit an advanced workflow, they do require users to be comfortable with simple concepts, such as:

* Controlling the flow of a workflow using [conditionals](../workflows/custom/conditionals.md)
* Specifying when workflows should run by customizing the workflow's [triggering event](../workflows/custom/triggers/index.md)
* Chaining [actions](../workflows/custom/actions/index.md) together to perform desired operations


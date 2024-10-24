## Creating workflows for call queues, IVR menus and voicemail-only extensions

To key to becoming a Workflow Builder expert lies in understanding how your account has been configured to route and handle calls. Lets suppose one wants to implement the following workflow: when a customer calls the main company number, if the call is missed, then I want to send the customer an SMS." 

It is entirely logical to think that to enable the above workflow, one needs to bind a workflow to the main company number. However, if your call handling rules route incoming calls to a call queue for example, or an IVR menu, then the correct course of action is to bind your workflows to those extensions -- and *not* directly to the main company number. 

!!! tip "A simple and effective trick is to create a simple diagram of your company's phone tree and call routing rules. Once you are able to visualize where calls are ultimately routed, then it becomes much easier to know which extensions to bind and setup workflows for."


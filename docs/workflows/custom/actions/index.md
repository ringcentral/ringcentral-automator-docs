# Workflow actions

A workflow's actions is what makes a workflow do something. Without actions, workflows are completely inert. 

## Action inputs

Each action requires input to function properly. These inputs govern what the action will do specifically within the general constraints of the action. Who will I send the SMS to? What number will I send an SMS from? What will be the message? And so forth...

## Action outputs

Some actions also produce output. Output within the context of an action means that the action will add "action variables" to the current workflow's context, making those values accessible to subsequent actions. 

A good example is the [transcribe action](transcribe.md). As input you reference a URL to a media file. When it is done executing, it adds the "Transcript" variable to the workflow's context, allowing you to reference the transcript later to send the transcript in an SMS, or to build [conditional logic](../flow/index.md) based upon the contents of the transcript. 

## List of available actions

<div class="grid cards actions" markdown>

- ![icon](../../../img/icon-action-comment.png){ .icon-node } __[Comment](comment.md)__
- ![icon](../../../img/icon-action-create-contact.png){ .icon-node } __[Create personal contact](create-contact.md)__
- ![icon](../../../img/icon-action-video.png){ .icon-node } __[Create meeting bridge](create-meeting.md)__
- ![icon](../../../img/icon-action-lookup-contact.png){ .icon-node } __[Lookup contact](lookup-contact.md)__
- ![icon](../../../img/icon-action-parse-json.png){ .icon-node } __[Parse JSON](parse-json.md)__
- ![icon](../../../img/icon-action-ringout.png){ .icon-node } __[Place RingOut call](ringout.md)__
- ![icon](../../../img/icon-action-send-chat.png){ .icon-node } __[Send chat message](send-chat-message.md)__
- ![icon](../../../img/icon-action-send-sms.png){ .icon-node } __[Send SMS](send-sms.md)__
- ![icon](../../../img/icon-action-http-request.png){ .icon-node } __[Send HTTP request](http-request.md)__
- ![icon](../../../img/icon-action-set-variable.png){ .icon-node } __[Set variable](set-variable.md)__
- ![icon](../../../img/icon-action-update-contact.png){ .icon-node } __[Update personal contact](update-contact.md)__

</div>

**Supported in Automator only**

The following nodes are currently only supported in RingCentral Automator, Workflow Builder's predecessor. 

<div class="grid cards actions" markdown>

- __[Transcribe media file](transcribe.md)__

</div>

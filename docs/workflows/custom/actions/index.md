# Workflow actions

A workflow's actions is what makes a workflow do something. Without actions, workflows are completely inert. 

## Action inputs

Each action requires input to function properly. These inputs govern what the action will do specifically within the general constraints of the action. Who will I send the SMS to? What number will I send an SMS from? What will be the message? And so forth...

## Action outputs

Some actions also produce output. Output within the context of an action means that the action will add "action variables" to the current workflow's context, making those values accessible to subsequent actions. 

A good example is the [transcribe action](transcribe.md). As input you reference a URL to a media file. When it is done executing, it adds the "Transcript" variable to the workflow's context, allowing you to reference the transcript later to send the transcript in an SMS, or to build [conditional logic](../conditionals.md) based upon the contents of the transcript. 

## List of available actions

* [Comment](comment.md)
* [Create personal contact](create-contact.md)
* [Create meeting bridge](create-meeting.md)
* [Exit](exit.md)
* [Lookup contact](lookup-contact.md)
* [Place RingOut call](ringout.md)
* [Send chat message](send-chat-message.md)
* [Send SMS](send-sms.md)
* [Send HTTP request](http-request.md)
* [Transcribe media file](transcribe.md)

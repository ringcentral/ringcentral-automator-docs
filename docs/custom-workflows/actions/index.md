# Workflow actions

A workflows actions is what makes an automation do something. Without actions, workflows are completely inert. 

## Action inputs

Each action requires input to function properly. These inputs govern what the action will do specifically within the general constraints of the action. Who will I send the SMS to? What number will I send an SMS from? What will be the message? And so forth...

## Action outputs

Some actions also produce output. Output within the context of an action means that the action will add "action variables" to the current automation's context, making those values accessible to subsequent actions. 

A good example is the [transcribe action](./transcribe/). As input you reference a URL to a media file. When it is done executing, it adds the "Transcript" variable to the automation's context, allowing you to reference the transcript later to send the transcript in an SMS, or to build [conditional logic](../conditionals/) based upon the contents of the transcript. 

## List of available actions

* [Comment](./comment/)
* [Create personal contact](./create-contact/)
* [Create meeting bridge](./create-meeting/)
* [Exit](./exit/)
* [Lookup contact](./lookup-contact/)
* [Place RingOut call](./ringout/)
* [Send chat message](./send-chat-message/)
* [Send SMS](./send-sms/)
* [Send HTTP request](./http-request/)
* [Transcribe media file](./transcribe/)

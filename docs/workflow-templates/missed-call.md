# Missed call auto-response

!!! info "Deprecated"
    This template is deprecated. Please refer to [the missed call recipe](../recipes/missed-call.md) for importing new missed call template.

This automation results in an SMS message being send to a caller whose call into a phone number or extension is missed. The term "missed call" has a specific technical meaning which is important to understand in order to employ this automation successfully. A "missed call" refers to a call in which a user hangs up prior to being connected to a logical terminus of a call flow. Let's explore some examples:

**Examples of missed calls**

* When a person is making a call to an extension user, and hangs up prior to being connected or went to voicemail.
* When a person is waiting in a call queue and hangs up prior to being connected

**These are NOT missed calls**

* When a person is connected to a voicemail, whether or not they leave a message
* When a person waits the designated amount of time in a call queue, and is automatically routed to another extension

The key to understanding a missed call lies in understanding the call handling rules. When a call handling rule is successfully engaged to route the call to another extension, then that is NOT a missed call, even if noone answers. 

## Configuration parameters

| Parameter | Description |
|-|-|
| **Enable this automation for what phone numbers?** | The list of phone numbers for which to enable this automation. |
| **Select the phone number your SMS will be sent from** | The phone number from which the auto-response will be sent. |
| **Auto-reply text** | The message to respond with. |

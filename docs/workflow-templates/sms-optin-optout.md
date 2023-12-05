# Opt-in/opt-out auto-response

!!! warning "**Important**"
    This automation only handles the SMS auto-response. It does not play any role in enforcing a person's wish not to receive SMS. It is incumbant upon the user of this automation to respect the subscription preferences stated by the sender. 

This automation helps users stay compliant with business SMS rules, and helps to prevent carriers from blocking or penalizing senders of SMS messages. This automation will send responses for two different scenarios: when a request is received to unsubscribe and to subscribe to text messages. 

To assist users in keeping track of people requesting to opt-out, this automation will create and/or update the address book entry associated with the sender of the SMS, and update the notes field associated with the address book entry stating that they have requested to opt-out or opt-in. 

**Opt-out keywords (case insensitive)**

* UNSUBSCRIBE
* STOP 

**Opt-in keywords (case insensitive)**

* SUBSCRIBE
* RESUBSCRIBE
* START

If you wish to customize the keywords this automation will respond to, convert the automation to an "advanced workflow" (see [Custom workflows](../custom-workflows/index.md) help section), and edit the appropriate conditional elements relating to keywords. 

## Configuration parameters

| Parameter | Description |
|-|-|
| **Enable this automation for what phone numbers?** | The list of phone numbers for which to enable this automation. |
| **Opt-in auto-reply text** | The message to be sent when a person opts-in to receiving SMS messages. |
| **Opt-out auto-reply text** | The message to be sent when a person opts-out of receiving SMS messages. |

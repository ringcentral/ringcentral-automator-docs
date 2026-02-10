# Forward all SMS 

The **Forward All SMS** recipe is a foundational workflow template designed to demonstrate how incoming SMS content can be automatically redirected to another destination. When active, this workflow intercepts every SMS received by your specified number and sends a copy of that message content to a secondary phone number.

This is particularly useful for ensuring that urgent client communications are not missed when you are away from your primary device or need to delegate message monitoring to a colleague.

## How it Works

When an SMS is received, the workflow captures the message body and the sender's information. It then initiates a new SMS task to "forward" that information to the target recipient.

### Operational Considerations

Because this workflow is designed to forward **ALL** incoming messages, users should manage its activation carefully:

* **Manual Control:** You must manually enable the workflow when you want forwarding to begin and disable it when it is no longer needed.
* **Time-Based Logic:** For a true "Out-of-Office" scenario, it is recommended to modify the imported workflow by adding a **Time Condition** step to ensure it only executes between specific start and end times.


!!! info "Important Limitations"
    It is vital to understand the technical behavior of SMS forwarding versus traditional call forwarding:

       * **Sender Identity:** Unlike a forwarded phone call, a forwarded SMS does not "spoof" the original sender's number. The recipient will see the message as coming **from your phone number**, not the original sender.
       * **Replying:** If the person receiving the forwarded message wishes to reply to the original sender, they cannot simply hit "Reply." They must manually compose a new message to the original sender's phone number.
       * **Loop Prevention:** Ensure you do not forward messages to a number that is also configured to forward back to you, as this can create an infinite loop of messages.

## Scaling Your Solution

If your goal is to have multiple people monitor and respond to the same set of incoming text messages, a simple forwarding workflow may not be the best fit.

For team-based collaboration, consider **RingCentral’s SMS Call Queue** feature (available as part of the [Customer Engagement Bundle](https://www.ringcentral.com/us/en/blog/unify-conversations-elevate-customer-engagement/)). This allows a group of users to share a common SMS identity, see conversation history, and reply collectively without the limitations of individual message forwarding.

[:fontawesome-solid-download: Download workflow](forward-sms.json){: download .md-button }

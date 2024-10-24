---
tags:
  - recipe
  - SMS
---

# Sending an SMS to users once, and only once

Let's say you want to set up an SMS autoresponse that is triggered whenever a new customer messages you for the first time. Perhaps you want to welcome them as a new customer, or perhaps you want to send them a disclaimer. Whatever the circumstance, we can achieve this through a workflow that utilizes the following logic:

* Whenever you receive an SMS, look up the sender's phone number in your address book. 
* If a contact is found, then do nothing.
* But if a contact is *not* found, then we can assume this is the first time they have messaged us. 
* Go ahead, and send your auto-reply message. 
* Finally, add the phone number to your address book so that the next time they send a message, they will short circuit the workflow and prevent it from messaging them again. 

[:fontawesome-solid-download: Download workflow](autoreply-only-once.json){: download .md-button }

Learn how to [import it into your account](../../users/import-export.md#importing-workflows). 



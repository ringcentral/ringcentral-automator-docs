---
tags:
  - recipe
  - Opt-out
  - Opt-in
  - SMS
  - Auto-reply
---

# Acknowledge reciept of an opt-out or opt-in request via SMS

!!! warning "**Opt-in and opt-out auto-replies is now supported in our core product**"
    This recipe is for demonstration purposes only and is meant to illustrate a way of implementing auto-responses to specific keywords. If you are in need of this specific feature we strongly recommend you setup your RingCentral account accordingly. 

This workflow is a good demonstration of how you can setup Workflow Builder to acknowledge the reciept of messages that contain specific keywords. It models the use case of sending SMS auto-replies in response to receiving specific commands or keywords. In addition, it demonstrates how to augment a contact record in RingCentral with a note to keep a record of the received correspondence. 

Once you install the recipe, if you wish to customize the keywords this workflow will respond to then edit the appropriate conditional elements relating to keywords in the advanced workflow. 

As a final reminder, RingCentral does not recommend using the recipe as-is. SMS opt-in and opt-out auto-responses are managed within our core product. Using this workflow will result in duplicated messages being sent and could increase your costs. 

[:fontawesome-solid-download: Download workflow](sms-optout-autoreply.json){: download .md-button }

Learn how to [import it into your account](../../users/import-export.md#importing-workflows). 

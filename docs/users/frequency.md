# Limiting the frequency of workflows

There are a number of scenarios in which one would like to limit how frequently a workflow is run. Consider the circumstance where I am on vacatation and have set up an auto-response saying, "I am on PTO and will reply to your message on [insert date]." Let's then say a customer begins texting me multitple times. I only want to reply once per day to tell them I am on PTO. That will help me save money, as every SMS message I send may come with a small cost, and it keeps the conversation with the customer clean.

To limit workflows in this way, to control how often they are run in response to a given event, look for following option found by editing a workflow, or by editing the trigger associated with an advanced workflow. 

![Workflow frequency settings](../img/automation-frequency.png){ style="max-width: 400px" }

Any limit you set will apply within the context of a given individual you are communicating with. For example, you can limit a workflow to run once per day per *phone number*. This means that if multiple people are texting you from multiple phone numbers, they will each receive your autoreply only once per day.


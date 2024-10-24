# Workflow histories

Every execution of a workflow is recorded for audit trail purposes. This allows you to see a history of when your workflow was triggered and executed, with some limited insights into what happened when the workflow was executed. 

For purposes related to data privacy and security, you will see limited data relating to data that triggered the workflow. If you would like to see more data in your execution history, use the "Comment" action in your workflow to log more data to the execution history. 

!!! info "Histories are only maintained for seven days"
    Workflow histories are only retained for seven days and exist primarily to help users troubleshoot and debug workflows they have created. RingCentral may retain a history of the workflow having run in different forms, e.g. the message store and a user's call log. 

#### Why is my workflow history empty?

A history record is only created if the triggering event passes through all of the attached filters of the workflow's trigger. In other words, if you have a workflow that is triggered by a missed call event, and a filter has been applied to that trigger that says, "only process this event if the caller's phone number does not start with '888'," then the workflow will only run if the caller's phone number does not start with 888. So while there was an event that was received by Workflow Builder, the workflow was never executed because the caller's phone number did not meet the trigger's filtering criteria. 


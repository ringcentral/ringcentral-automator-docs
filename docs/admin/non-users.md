# Managing workflows for call queues and other extension types

For Call Queue, Voicemail, IvrMenu and Park Location extension types, workflows are run on behalf of the person who created the workflow by default. In other words, if you were to inspect your company’s audit trail, the creator of the workflow would be seen as the user who performed the actions within the workflow. Administrators can specify another user to run a workflow on behalf of. This may give one workflow access to features and phone numbers they might otherwise not have access to.

1. the left-hand navigation, open "Extensions" section, and select extension
2. Create and edit workflows for the selected extension

![manage-extensions](../img/manage-extensions.png)

!!! info "For IvrMenu extensions, only the [call received](../workflows/custom/triggers/call-received.md) and [call ended](../workflows/custom/triggers/call-ended.md) triggers are supported. The [missed call event](../workflows/custom/triggers/call-missed.md) is not supported for IvrMenu." 

!!! info "Only most recent ten users will be displayed"
    During the beta, only the most recently added ten users will be listed in your list of users/extensions. If you have more than ten active users, they are still in the system, and their workflows will continue to run even if they are not in your list of users. You may always add them back to your list of users if you need to view or manage their workflows on their behalf.

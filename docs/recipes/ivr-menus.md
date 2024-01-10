# Triggering automations within an IVR menu

For IvrMenu extensions, only call received and call ended trigger are supported. Missed call event is not supported for IvrMenu. 

For "Call ended", there is a variable "Call end reason" that can know if user end the call before pressing a key. For example, let's say you have an IVR menu that prompts people with, "Press 1 to speak to Sales, press 2 to leave a voicemail." When user end the call without pressing any key, "Call end reason" will be "CallerDropped". But when user is redirected by pressing 1, "Call end reason" will be "NoReason". For now, we can't know which key user press.


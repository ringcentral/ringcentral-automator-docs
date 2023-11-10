# Action: create meeting bridge

Creates a meeting bridge in which a meeting can take place. A meeting "bridge" is RingCentral parlance for a meeting room or meeting URL. When you create a bridge, you will obtain through the action's output, a URL that when clicked on will start a meeting. 

!!! info "How do I specify a meeting start and end time?"
    You may notice that you do not need to provide a date and time in order to create a meeting. That is because RingCentral delegates the schedule of a meeting exclusively to the calendaring system in which a meeting URL is inserted. Therefore, all this action will do is generate a room in which a meeting will occur, and provide that URL to you as output so that you can transmit to a person or external system.

## Input

| Variable                                | Type    | Description                                                 |
|-----------------------------------------|---------|-------------------------------------------------------------|
| **Meeting name**                        | String  | The name of the meeting                                     |
| **Meeting password**                    | String  | The password required to access the meeting.                |
| **Participants can only join after me** | boolean | An option to not start the meeting until the host arrives.  |
| **Enable waiting room for**             | boolean | An option to determine whom will be placed in a waiting room prior to the start of the meeting. |

## Output

| Variable         | Type | Description                                 |
|------------------|------|---------------------------------------------|
| **Meeting link** | URL  | The meeting bridge's fully-formed join URL. |

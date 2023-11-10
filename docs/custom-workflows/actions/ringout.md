# Action: place call (via RingOut)

Initiates a phone call between two parties using the RingOut protocol. The RingOut protocol works by calling the caller (the person initiating the call). When the caller answers the phone, the other party to the phone call is then called. When the intended recipient answers, the two parties are then connected. 

## Input

| Variable                           | Type         | Description                                                               |
|------------------------------------|--------------|---------------------------------------------------------------------------|
| **Originating phone number**       | Phone number | The phone number of the caller.                                           |
| **Recipient phone number**         | Phone number | The phone number of the callee, or recipient of the caller's call.        |
| **Prompt before connecting calls** | boolean      | An option to prompt the caller to press "1" prior to calling the caller.  |

## Output

None.

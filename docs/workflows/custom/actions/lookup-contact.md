# Action: lookup contact

Looks up a contact in your RingCentral address book, both your internal company directory, as well as your personal address book. 

When combined with the "create contact" action, this is very helpful in creating customized responses based upon whether you have previously corresponded with an individual. It is also useful to be able to disambiguate between internal communications (does the person sending me an SMS have an entry within our internal company directory?) and external or customer communications. 

There is no guarantee that every output variable will contain a value. What gets returned depends upon what data is stored for that contact. 

## Input

| Variable         | Type         | Description                          |
|------------------|--------------|--------------------------------------|
| **Phone number** | Phone number | Looks up a contact by phone number.  |

## Output

| Variable         | Type         | Description                          |
|------------------|--------------|--------------------------------------|
| **Contact exists** | boolean | "True" if the phone number was found in any address book, and "false" otherwise. |
| **Is personal contact** | boolean | "True" if the phone number was found in the current user's personal address book, and "false" otherwise. |
| **Is from company directory** | boolean | "True" if the phone number was found in the current account's company directory, and "false" otherwise. This typically signifies a co-worker. |
| **Contact first name** | String | |
| **Contact last name** | String | |
| **Contact name** | String | |
| **Contact email** | Email | |
| **Contact company** | String | |
| **Contact job title** | String | |
| **Contact business phone** | Phone number | |
| **Contact home phone** | Phone number | |
| **Contact mobile phone** | Phone number | |
| **Contact company phone** | Phone number | |
| **Contact assistant phone** | Phone number | |
| **Contact other phone** | Phone number | |
| **Contact primary phone** | Phone number | |
| **Contact business phone** | Phone number | |
| **Contact business address street** | String | |
| **Contact business address city** | String | |
| **Contact business address state** | String | |
| **Contact business address zip** | String | |


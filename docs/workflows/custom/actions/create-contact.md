# Action: create personal contact

Creates a new record within the current user's personal address book. 

!!! info "Personal address book limitations"
    Workflow Builder does not have the ability to create records within a company's primary directory, as that is most often managed externally to RingCentral. One is only able to add record's to their personal address book. Therefore, bear in mind that every user has their own address book. 

## Input

| Variable               | Type         | Description                                                               |
|------------------------|--------------|---------------------------------------------------------------------------|
| **First name**         | String       | This value will be assigned to the contact's first name property.         |
| **Last name**          | String       | This value will be assigned to the contact's last name property.          |
| **Email**              | Email        | This value will be assigned to the contact's email property.              |
| **Phone number**       | Phone number | This value will be assigned to the contact's phone number property.       |
| **Phone number label** | Phone number | This value will be assigned to the contact's phone number label property. |
| **Company**            | String       | This value will be assigned to the contact's company property.            |
| **Notes**              | String       | This value will be assigned to the contact's notes property.              |

## Output

None. 

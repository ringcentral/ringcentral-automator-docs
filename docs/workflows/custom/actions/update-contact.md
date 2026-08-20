# Action: update personal contact

Updates an existing record in the current user's personal address book. Use the [lookup contact](lookup-contact.md) action first to find the personal contact and obtain its contact ID.

!!! info "Personal address book limitations"
    Workflow Builder can update contacts in the workflow owner's personal address book, but it cannot update records in the company directory.

## Input

| Variable               | Type         | Description                                                               |
|------------------------|--------------|---------------------------------------------------------------------------|
| **Contact ID**         | String       | Identifies the personal contact to update.                                |
| **First name**         | String       | Updates the contact's first name.                                         |
| **Last name**          | String       | Updates the contact's last name.                                          |
| **Email**              | Email        | Updates the contact's email address.                                      |
| **Phone number**       | Phone number | Updates the contact's phone number.                                       |
| **Phone number label** | String       | Identifies the type of phone number, such as business, mobile, or home.    |
| **Company**            | String       | Updates the contact's company.                                            |
| **Notes**              | String       | Updates the contact's notes.                                              |

## Output

None.

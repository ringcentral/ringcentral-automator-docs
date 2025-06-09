# Trigger: Fax received

This event is fired when the current user receives a fax via any of the phone numbers they have access to. 

## Viewing Fax Content

When a fax is sent or received, the associated trigger event includes a variable named Fax attachment URI. This variable provides a direct URL to the fax message media.

### Direct Media Access

The Fax attachment URI variable contains the raw URL to the fax media file. For example:

> https://media.ringcentral.com/restapi/v1.0/account/170xxx004/recording/6571972004/content

You can use this URL to directly access the fax content, which is typically in a format like TIFF.

### Constructing a Viewable URL

To provide a user-friendly way to view the fax content directly in a web browser, you can construct a special URL using the RingCentral Media Reader. This reader is a web-based tool that can interpret and display various media types, including faxes.

To construct a viewable URL, prepend the Fax attachment URI with the RingCentral Media Reader URL:

> https://ringcentral.github.io/ringcentral-media-reader/index.html?media=

Combining this with the Fax attachment URI results in a clickable URL like this:

> https://ringcentral.github.io/ringcentral-media-reader/index.html?media=https://media.ringcentral.com/restapi/v1.0/account/170xxx004/recording/6571972004/content

By providing users with such a URL, they can easily click to open and view the fax content within their browser.

## Trigger variables

| Trigger variable | Type | Description |
|-|-|-|
| **Sender's phone number** | Phone number | The phone number that sent the fax that was received in E.164 format. |
| **Sender's name** | String | If the sender exists in your address book, this variable will contain the name stored in your address book. | **Recipient's phone number** | Phone number | The phone number that received the fax in E.164 format. |
| **Fax read status** | String | Whether or not the fax has been marked as read via the RingCentral application. Possible values: "Read" or "Unread" |
| **Fax priority** | String | Possible values: "Normal" or "High" |
| **Fax attachment URI** | String | The URL which a user can click to view the received fax within RingCentral. |
| **Fax attachment content type** | String | The content-type of the received fax. |
| **Fax subject** | String | The subject of the fax. |
| **Fax resolution** | String | The graphical resolution of the received fax. Possible values: "Low" or "High" |
| **Fax page count** | integer | The number of pages received. |
| **Fax direction** | String | Possible values: "Inbound" or "Outbound." |
| **Fax received date** | date | The date the message was received, in the format of YYYY-MM-DD. |
| **Fax received time** | time | The time the message was received, in the format of HH:MM:SS (AM|PM) | 
| **Fax received date time** | timestamp | The combined date and time of a received fax, in the format of YYYY-MM-DD HH:MM:SS (AM|PM) |
| **Fax received day of week** | day of the week | The day of the week the fax was received. |
| **Fax received localized date time** | time | The combined date and time of a received fax, expressed in the user's preferred timezone. |
| **Fax message status** | String | This is always equal to "Received" for this trigger. |
| **Fax sender's formatted phone number** | String | A formatted version of the sender's phone number. |


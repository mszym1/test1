

# Header1
Represents a request for a meeting in a calendar.

| Element | Description | Type | Required | Notes |
|---- | --- | --- | --- | --- |
| meeting | Top level | meeting data object | Required | |
| <p align="left">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;time</p> | When meeting starts. [Header2](#Header2)  | string | Required | Format is YYYY-MM-DD HH:MM:SS. Timezone is GMT. |
| <p align="left">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;duration</p> | How long meeting lasts | number | Required | In minutes |
| &nbsp; &nbsp; &nbsp; &nbsp; description | Description of the meeting | string | Required | |
| &nbsp; &nbsp; &nbsp; &nbsp; location | Location of the meeting | number | Optional | Default is an empty string |
| &nbsp; &nbsp; &nbsp; &nbsp; reminder | How many minutes before the meeting a reminder event should take place | number | Optional | Default is 10 minutes |
| &nbsp; &nbsp; &nbsp; &nbsp; invitees | List of email address of people to invite to the meeting | array of string | Optional | The strings should be valid email addresses. Default is an empty array. |

# Header2

Represents a request to record a television program.

| Element | Description | Type | Required | Notes |
| --- | --- | --- | --- | --- |
| recordTV | Top level | TV program data | Required | |
| &nbsp; &nbsp; date | Date of the program | string | Optional | Format is YYYY-MM-DD HH:MM:SS. Default value is today's date. |
| &nbsp; &nbsp; time | Time the program begins | number | Required | Attributes: **format** has values `24` or `12` for 24 or 12 hour formats. Format is HH:MM, with am or pm afterwards for 12 hour format |
| &nbsp; &nbsp; duration | Length of the program | number | Required | In hours |
| &nbsp; &nbsp; channel | Channel to record | number | Required | |


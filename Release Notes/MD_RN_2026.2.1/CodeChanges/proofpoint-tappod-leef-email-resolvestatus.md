# Code Changes for proofpoint-tappod-leef-email-resolvestatus (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['"rcpts"+:\s*\[({email_recipients}"+({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"*[^\]]*?)\]'] |
| edit_regex_field | email_recipients |  | ['"rcpts"+:\s*\[({email_recipients}"+({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"*[^\]]*?)\]'] |
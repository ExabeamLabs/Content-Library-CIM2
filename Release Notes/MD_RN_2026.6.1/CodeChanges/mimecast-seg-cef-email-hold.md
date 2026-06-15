# Code Changes for mimecast-seg-cef-email-hold (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['"(recipientAddress|Recipient)":"({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)'] |
| edit_regex_field | email_address |  | ['(senderAddress|Sender)":"(<>|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)(?<!loc)(?<!prd)(?<!localdomain))"'] |
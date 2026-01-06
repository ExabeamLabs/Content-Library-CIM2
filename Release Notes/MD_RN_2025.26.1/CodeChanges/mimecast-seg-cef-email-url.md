# Code Changes for mimecast-seg-cef-email-url (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'category', 'dest_email_address', 'direction', 'email_address', 'email_subject', 'failure_reason', 'message_id', 'operation', 'result', 'service_name', 'src_ip', 'time', 'url'] |
| edit_regex_field | email_address |  | ['"+fromUserEmailAddress"+:"+({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"'] |
| added_regex_field | dest_email_address |  | ['"+userEmailAddress"+:"+({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"'] |
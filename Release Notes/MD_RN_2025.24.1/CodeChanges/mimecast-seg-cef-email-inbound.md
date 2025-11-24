# Code Changes for mimecast-seg-cef-email-inbound (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'bytes', 'category', 'dest_email_address', 'direction', 'email_address', 'email_attachment', 'email_domain', 'email_subject', 'email_user', 'message_id', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | dest_email_address |  | ['"(recipientAddress|Recipient)":"({email_user}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))'] |
| added_regex_field | email_user |  | ['"(recipientAddress|Recipient)":"({email_user}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))'] |
| removed_attribute | DupFields |  | N/A |
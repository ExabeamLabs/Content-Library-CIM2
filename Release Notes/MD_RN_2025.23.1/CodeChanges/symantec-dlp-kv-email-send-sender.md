# Code Changes for symantec-dlp-kv-email-send-sender (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_type', 'dest_email_address', 'dest_email_domain', 'email_address', 'email_attachment', 'email_attachments', 'email_domain', 'email_recipients', 'email_subject', 'host', 'message_id', 'result', 'time'] |
| added_regex_field | message_id |  | ['Message_ID:\_({message_id}[^\s]+)'] |
| removed_attribute | DupFields |  | N/A |
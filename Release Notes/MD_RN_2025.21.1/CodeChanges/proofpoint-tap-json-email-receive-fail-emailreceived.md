# Code Changes for proofpoint-tap-json-email-receive-fail-emailreceived (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'bytes', 'country', 'creator', 'dest_email_address', 'dest_email_domain', 'dest_ip', 'dest_port', 'direction', 'email_address', 'email_attachment', 'email_attachments', 'email_domain', 'email_recipients', 'email_subject', 'folder_name', 'host', 'is_consolidated', 'message_id', 'page_count', 'result', 'rule', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | email_attachment |  | ["'detectedName':\s*'({email_attachments}({email_attachment}[^']+))"] |
| added_regex_field | email_attachments |  | ["'detectedName':\s*'({email_attachments}({email_attachment}[^']+))"] |
| removed_attribute | DupFields |  | N/A |
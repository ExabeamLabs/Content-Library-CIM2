# Code Changes for microsoft-o365-json-email-send-receive-internentmessageid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_type', 'app', 'attachment', 'dest_email_address', 'direction', 'email_address', 'email_recipients', 'email_subject', 'email_user', 'file_ext', 'file_name', 'hash_sha256', 'src_ip', 'src_port', 'time', 'user_type', 'verdict'] |
| edit_regex_field | email_subject |  | ['"Subject":"\s*({additional_info}({email_subject}[^"]+?))\s*",'] |
| added_regex_field | additional_info |  | ['"Subject":"\s*({additional_info}({email_subject}[^"]+?))\s*",'] |
| removed_attribute | DupFields |  | N/A |
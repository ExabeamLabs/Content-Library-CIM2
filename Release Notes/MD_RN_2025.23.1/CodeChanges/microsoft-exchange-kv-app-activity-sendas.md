# Code Changes for microsoft-exchange-kv-app-activity-sendas (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'domain', 'email_address', 'email_attachment', 'email_attachments', 'email_domain', 'email_subject', 'host', 'object', 'operation', 'path', 'process_path', 'result', 'src_ip', 'src_port', 'target', 'time', 'user', 'user_sid'] |
| edit_regex_field | email_attachments |  | ['\"Attachments\\*\"+:[\s\\]*\"+\s*({additional_info}({email_attachments}[^\"\\]+))\s*'] |
| edit_regex_field | email_subject |  | ['\"Subject\":\"\s*({object}({email_subject}[^\"}]+?))\s*\"'] |
| added_regex_field | additional_info |  | ['\"Attachments\\*\"+:[\s\\]*\"+\s*({additional_info}({email_attachments}[^\"\\]+))\s*'] |
| added_regex_field | object |  | ['\"Subject\":\"\s*({object}({email_subject}[^\"}]+?))\s*\"'] |
| removed_attribute | DupFields |  | N/A |
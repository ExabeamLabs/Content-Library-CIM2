# Code Changes for proofpoint-tap-json-email-emailthreat (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_type', 'bytes', 'dest_email_address', 'dest_email_domain', 'direction', 'email_address', 'email_attachment', 'email_attachments', 'email_domain', 'email_recipients', 'email_subject', 'file_name', 'malware_url', 'message_id', 'mime', 'result', 'src_ip', 'src_port', 'threat_url', 'time'] |
| edit_regex_field | email_attachment |  | ['"filename\\":\s*\\"({email_attachments}({file_name}({email_attachment}[^"]+)))?\\"'] |
| edit_regex_field | malware_url |  | ['"threat\\":\s*\\"({additional_info}({malware_url}[^"]+\.\w+\/?[^"]+))\\"'] |
| added_regex_field | additional_info |  | ['"threat\\":\s*\\"({additional_info}({malware_url}[^"]+\.\w+\/?[^"]+))\\"'] |
| added_regex_field | email_attachments |  | ['"filename\\":\s*\\"({email_attachments}({file_name}({email_attachment}[^"]+)))?\\"'] |
| added_regex_field | file_name |  | ['"filename\\":\s*\\"({email_attachments}({file_name}({email_attachment}[^"]+)))?\\"'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for mimecast-seg-cef-email-hold (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'category', 'dest_email_address', 'direction', 'dproc', 'email_address', 'email_attachment', 'email_subject', 'file_ext', 'file_hash', 'file_name', 'file_type', 'message_id', 'result', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | email_attachment |  | ['"fileName":"({file_name}({email_attachment}[^"]+\.({file_ext}[^"]+)))'] |
| edit_regex_field | file_ext |  | ['"fileName":"({file_name}({email_attachment}[^"]+\.({file_ext}[^"]+)))'] |
| added_regex_field | file_name |  | ['"fileName":"({file_name}({email_attachment}[^"]+\.({file_ext}[^"]+)))'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for tessian-dlp-email-alert (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_severity', 'alert_type', 'bcc', 'bytes', 'cc', 'dest_email_address', 'email_address', 'email_attachment', 'email_attachments', 'email_recipients', 'email_subject', 'message_id', 'result', 'time'] |
| edit_regex_field | alert_name |  | ['"tessian_action":"({alert_type}({alert_name}[^"]+))"', '"threat_types":\["({alert_type}({alert_name}[^"]+))"\]'] |
| added_regex_field | alert_type |  | ['"tessian_action":"({alert_type}({alert_name}[^"]+))"', '"threat_types":\["({alert_type}({alert_name}[^"]+))"\]'] |
| removed_attribute | DupFields |  | N/A |
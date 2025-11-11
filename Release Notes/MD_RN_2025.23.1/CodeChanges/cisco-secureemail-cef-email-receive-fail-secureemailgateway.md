# Code Changes for cisco-secureemail-cef-email-receive-fail-secureemailgateway (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_email_address', 'dest_email_domain', 'direction', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'host', 'result', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | action |  | ['\Wact=({result}({action}[^=]+?))\s*\w+='] |
| added_regex_field | result |  | ['\Wact=({result}({action}[^=]+?))\s*\w+='] |
| removed_attribute | DupFields |  | N/A |
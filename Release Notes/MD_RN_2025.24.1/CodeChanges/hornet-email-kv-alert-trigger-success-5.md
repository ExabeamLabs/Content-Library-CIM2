# Code Changes for hornet-email-kv-alert-trigger-success-5 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_email_address', 'dest_email_domain', 'dest_host', 'dest_ip', 'direction', 'domain', 'email_address', 'email_attachments', 'email_domain', 'email_subject', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | alert_type |  | ['type=({alert_severity}({alert_type}5))'] |
| added_regex_field | alert_severity |  | ['type=({alert_severity}({alert_type}5))'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for microsoft-o365-cef-alert-trigger-success-alertdetected (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'app', 'dest_email_address', 'dest_email_domain', 'email_address', 'email_domain', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'operation', 'process_name', 'src_host', 'src_ip', 'src_port', 'target', 'time', 'user', 'user_id'] |
| edit_regex_field | alert_name |  | ['"PolicyName":"({alert_subject}({event_name}({alert_name}[^"]+)))"'] |
| edit_regex_field | dest_email_address |  | ['"ToPerson":"({target}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"'] |
| edit_regex_field | dest_email_domain |  | ['"ToPerson":"({target}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"'] |
| added_regex_field | alert_subject |  | ['"PolicyName":"({alert_subject}({event_name}({alert_name}[^"]+)))"'] |
| added_regex_field | event_name |  | ['"PolicyName":"({alert_subject}({event_name}({alert_name}[^"]+)))"'] |
| added_regex_field | target |  | ['"ToPerson":"({target}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"'] |
| removed_attribute | DupFields |  | N/A |
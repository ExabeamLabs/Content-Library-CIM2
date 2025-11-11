# Code Changes for microsoft-exchange-json-email-send-originating (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'alert_type', 'bytes', 'dest_host', 'dest_ip', 'dest_port', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'num_recipients', 'return_path', 'src_host', 'src_ip', 'src_port', 'time'] |
| added_regex_field | alert_type |  | ['exchange_source":"(?:|({alert_type}[^"]+))",'] |
| removed_attribute | DupFields |  | N/A |
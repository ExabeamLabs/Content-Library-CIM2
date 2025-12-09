# Code Changes for checkpoint-ia-kv-endpoint-login-success-iaevents (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['action:"Log In"', 'product:"Identity Awareness"'] |
| changed_parsed_fields | N/A |  | ['action', 'direction', 'domain', 'end_time', 'event_name', 'full_name', 'host', 'identity_type', 'rule', 'rule_id', 'severity', 'src_host', 'src_ip', 'src_port', 'start_time', 'time', 'user'] |
| edit_regex_field | time |  | ['"*\s*time:"*({time}\d{10})'] |
| added_regex_field | src_host |  | ['src_machine_name:"({src_host}[^"]+)'] |
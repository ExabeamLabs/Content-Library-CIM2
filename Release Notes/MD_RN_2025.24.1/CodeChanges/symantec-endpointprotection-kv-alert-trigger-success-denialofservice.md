# Code Changes for symantec-endpointprotection-kv-alert-trigger-success-denialofservice (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'host', 'priority', 'protocol', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | alert_severity |  | ['(<({alert_severity}({priority}\d+))>)\w+\s+\d+\s+\d+:\d+:\d+\s*\w+\s+SymantecServer:'] |
| added_regex_field | priority |  | ['(<({alert_severity}({priority}\d+))>)\w+\s+\d+\s+\d+:\d+:\d+\s*\w+\s+SymantecServer:'] |
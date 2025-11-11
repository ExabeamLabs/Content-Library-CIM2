# Code Changes for cisco-fp-json-alert-trigger-success-connectiontimestamp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_description', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app_id', 'app_protocol', 'block_type', 'blocked', 'bytes', 'classification_name', 'connection_counter', 'dest_country', 'dest_ip', 'dest_port', 'device_id', 'egress_security_zone', 'host', 'impact', 'ingress_interface', 'ingress_zone', 'ioc_number', 'ip_protocol_id', 'policy_name', 'process_name', 'protocol', 'record_type', 'result', 'rule_id', 'sensor', 'src_country', 'src_ip', 'src_port', 'time', 'user', 'user_id'] |
| edit_regex_field | blocked |  | ['"blocked":\s*"({result}({blocked}[^"]+?))"', '"blocked":\s*({result}({blocked}[^",]+))'] |
| edit_regex_field | classification_name |  | ['"classificationName":\s*"({alert_type}({classification_name}[^"]+))'] |
| edit_regex_field | host |  | ['"sensor":\s*"({sensor}({host}[^"]+?))"', '"sensor":\s*"[^"]+?\s+-\s+({sensor}({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))"', '\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD', 'exa_json_path=$.@computed.sensor,exa_regex=[^"]+?\s+-\s({sensor}({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))'] |
| added_regex_field | alert_type |  | ['"classificationName":\s*"({alert_type}({classification_name}[^"]+))'] |
| added_regex_field | result |  | ['"blocked":\s*"({result}({blocked}[^"]+?))"', '"blocked":\s*({result}({blocked}[^",]+))'] |
| added_regex_field | sensor |  | ['"sensor":\s*"({sensor}({host}[^"]+?))"', '"sensor":\s*"[^"]+?\s+-\s+({sensor}({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))"', 'exa_json_path=$.@computed.sensor,exa_regex=[^"]+?\s+-\s({sensor}({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))'] |
| removed_attribute | DupFields |  | N/A |
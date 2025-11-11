# Code Changes for checkpoint-ngfw-kv-network-traffic-success-accept-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'app_protocol', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_name', 'full_name', 'host', 'protocol', 'rule', 'rule_uid', 'src_host', 'src_ip', 'src_port', 'src_translated_ip', 'user'] |
| added_regex_field | event_name |  | ['\WAction="({event_name}[^"]+)"'] |
| removed_attribute | DupFields |  | N/A |
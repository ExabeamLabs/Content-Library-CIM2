# Code Changes for checkpoint-ngfw-kv-app-notification-systemmonitor (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'action', 'additional_info', 'app_protocol', 'bytes', 'dest_host', 'dest_ip', 'dest_port', 'dest_translated_ip', 'dest_translated_port', 'domain', 'event_name', 'failure_reason', 'first_name', 'full_name', 'host', 'last_name', 'operation', 'origin_ip', 'origin_name', 'product_name', 'protocol', 'result', 'rule', 'rule_id', 'src_host', 'src_ip', 'src_port', 'src_translated_ip', 'src_translated_port', 'time', 'user'] |
| added_regex_field | event_name |  | ['\Waction:"({event_name}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |
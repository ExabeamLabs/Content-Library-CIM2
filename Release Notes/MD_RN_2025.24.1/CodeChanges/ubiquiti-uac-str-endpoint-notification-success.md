# Code Changes for ubiquiti-uac-str-endpoint-notification-success (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'device_name', 'event_name', 'firmware_version', 'host', 'operation', 'product_name', 'src_ip', 'src_mac', 'src_port'] |
| edit_regex_field | device_name |  | ['({product_name}({device_name}UAP-AC.+?))\-({firmware_version}\d+\.\d+[^\s:]+)'] |
| edit_regex_field | event_name |  | ['({operation}({event_name}ntpd: timed out))'] |
| edit_regex_field | firmware_version |  | ['({product_name}({device_name}UAP-AC.+?))\-({firmware_version}\d+\.\d+[^\s:]+)'] |
| added_regex_field | operation |  | ['({operation}({event_name}ntpd: timed out))'] |
| added_regex_field | product_name |  | ['({product_name}({device_name}UAP-AC.+?))\-({firmware_version}\d+\.\d+[^\s:]+)'] |
| removed_attribute | DupFields |  | N/A |
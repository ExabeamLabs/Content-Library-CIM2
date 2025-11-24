# Code Changes for ubiquiti-uac-str-endpoint-notification-success-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'device_name', 'event_category', 'event_id', 'firmware_version', 'host', 'product_name', 'src_mac', 'sub_category'] |
| edit_regex_field | device_name |  | ['({product_name}({device_name}UAP-AC.+?))\-({firmware_version}\d+\.\d+[^\s:]+)'] |
| edit_regex_field | firmware_version |  | ['({product_name}({device_name}UAP-AC.+?))\-({firmware_version}\d+\.\d+[^\s:]+)'] |
| added_regex_field | product_name |  | ['({product_name}({device_name}UAP-AC.+?))\-({firmware_version}\d+\.\d+[^\s:]+)'] |
| removed_attribute | DupFields |  | N/A |
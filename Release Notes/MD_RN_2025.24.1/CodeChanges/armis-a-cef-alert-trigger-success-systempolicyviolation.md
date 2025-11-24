# Code Changes for armis-a-cef-alert-trigger-success-systempolicyviolation (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_severity', 'alert_status', 'alert_type', 'device_1_category', 'device_1_id', 'device_1_model', 'device_1_name', 'device_1_sensor', 'device_1_severity', 'device_1_src_ip', 'device_1_type', 'device_category', 'device_id', 'device_id_list', 'device_model', 'device_name', 'device_type', 'sensor', 'severity', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | device_name |  | ['"device_0_name":"({src_host}({device_name}[^"]+))'] |
| added_regex_field | src_host |  | ['"device_0_name":"({src_host}({device_name}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |
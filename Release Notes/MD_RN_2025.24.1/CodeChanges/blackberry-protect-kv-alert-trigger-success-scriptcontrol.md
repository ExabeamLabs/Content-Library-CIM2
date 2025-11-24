# Code Changes for blackberry-protect-kv-alert-trigger-success-scriptcontrol (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_type', 'host', 'malware_file_name', 'malware_url', 'src_host', 'time', 'user'] |
| edit_regex_field | malware_url |  | ['File Path:\s*({malware_file_name}({malware_url}[^,]+))\s*,'] |
| added_regex_field | malware_file_name |  | ['File Path:\s*({malware_file_name}({malware_url}[^,]+))\s*,'] |
| removed_attribute | DupFields |  | N/A |
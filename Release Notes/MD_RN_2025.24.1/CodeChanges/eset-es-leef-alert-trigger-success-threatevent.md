# Code Changes for eset-es-leef-alert-trigger-success-threatevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'circumstances', 'dest_host', 'domain', 'engine_version', 'firstseen', 'hash_sha256', 'host', 'malware_url', 'object_type', 'process_dir', 'process_name', 'process_path', 'result_code', 'src_ip', 'src_port', 'threat_category', 'threat_handled', 'time', 'user'] |
| edit_regex_field | action |  | ['actionTaken=({additional_info}({action}[^=]+?))\s*(\w+=|$)'] |
| edit_regex_field | host |  | ['deviceName=({dest_host}({host}[^\s]+))\s'] |
| added_regex_field | additional_info |  | ['actionTaken=({additional_info}({action}[^=]+?))\s*(\w+=|$)'] |
| added_regex_field | dest_host |  | ['deviceName=({dest_host}({host}[^\s]+))\s'] |
| removed_attribute | DupFields |  | N/A |
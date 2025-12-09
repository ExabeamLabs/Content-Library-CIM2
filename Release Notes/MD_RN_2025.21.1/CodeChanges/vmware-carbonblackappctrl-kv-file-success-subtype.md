# Code Changes for vmware-carbonblackappctrl-kv-file-success-subtype (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'additional_info', 'alert_severity', 'dest_ip', 'dest_port', 'domain', 'event_name', 'file_ext', 'file_hash', 'file_name', 'file_path', 'host', 'operation', 'policy_name', 'process_dir', 'process_name', 'process_path', 'time', 'user'] |
| edit_regex_field | event_name |  | ['\ssubtype="({access}({event_name}[^"]+))"'] |
| added_regex_field | access |  | ['\ssubtype="({access}({event_name}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for microsoft-evsecurity-cef-ds-object-activity-success-4662 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object', 'object_name', 'object_server', 'object_type', 'operation', 'src_ip', 'src_mac', 'src_port', 'time', 'user'] |
| edit_regex_field | object_name |  | ['fname=({object}({object_name}[^\s]+))'] |
| added_regex_field | object |  | ['fname=({object}({object_name}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for microsoft-evsecurity-kv-ds-object-activity-success-5137-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['correlation_id', 'dest_host', 'domain', 'ds_name', 'ds_object_dn', 'ds_object_ou', 'ds_type', 'event_code', 'event_name', 'host', 'login_id', 'object_id', 'object_type', 'time', 'user'] |
| edit_regex_field | host |  | ['ComputerName=({dest_host}({host}[\w.\-]+))'] |
| added_regex_field | dest_host |  | ['ComputerName=({dest_host}({host}[\w.\-]+))'] |
| removed_attribute | DupFields |  | N/A |
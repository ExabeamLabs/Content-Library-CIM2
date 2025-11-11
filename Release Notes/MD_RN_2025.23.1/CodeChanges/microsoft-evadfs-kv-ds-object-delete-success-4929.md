# Code Changes for microsoft-evadfs-kv-ds-object-delete-success-4929 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'host', 'naming_context', 'object_name', 'operation_type', 'options', 'result_code', 'src_host', 'time'] |
| edit_regex_field | host |  | ['ComputerName(:|=)\s*({dest_host}({host}[\w.-]+))'] |
| added_regex_field | dest_host |  | ['ComputerName(:|=)\s*({dest_host}({host}[\w.-]+))'] |
| removed_attribute | DupFields |  | N/A |
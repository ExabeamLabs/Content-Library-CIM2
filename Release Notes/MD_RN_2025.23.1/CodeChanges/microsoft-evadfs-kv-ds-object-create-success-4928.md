# Code Changes for microsoft-evadfs-kv-ds-object-create-success-4928 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'ds_object_dn', 'event_code', 'host', 'naming_context', 'operation_type', 'options', 'result_code', 'src_ds_object_dn', 'src_host', 'time'] |
| edit_regex_field | host |  | ['ComputerName(:|=)\s*({dest_host}({host}[\w.-]+))'] |
| added_regex_field | dest_host |  | ['ComputerName(:|=)\s*({dest_host}({host}[\w.-]+))'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for microsoft-evsecurity-mix-ds-object-modify-success-5136 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['attribute', 'dest_host', 'domain', 'ds_object_dn', 'ds_object_ou', 'event_code', 'event_name', 'host', 'login_id', 'object_type', 'time', 'user'] |
| edit_regex_field | host |  | ['"ComputerName":"({dest_host}({host}[\w\-.]+))', '(Information|Success Audit|Audit Success)\s+({host}[^\s]+)'] |
| added_regex_field | dest_host |  | ['"ComputerName":"({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |
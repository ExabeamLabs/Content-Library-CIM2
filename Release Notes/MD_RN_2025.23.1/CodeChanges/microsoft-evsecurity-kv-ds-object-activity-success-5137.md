# Code Changes for microsoft-evsecurity-kv-ds-object-activity-success-5137 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'ds_object_dn', 'ds_object_ou', 'event_code', 'event_name', 'host', 'login_id', 'object_type', 'time', 'user'] |
| edit_regex_field | host |  | ['(Information|Success Audit|Audit Success)\s+({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['(Information|Success Audit|Audit Success)\s+({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |
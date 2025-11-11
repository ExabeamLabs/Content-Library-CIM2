# Code Changes for microsoft-evsecurity-json-ds-object-modify-success-5136-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'domain', 'ds_object_dn', 'ds_object_ou', 'event_code', 'event_name', 'host', 'login_id', 'object_type', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['"HostID":"({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['"HostID":"({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for helpsystems-piam-kv-user-switch-success-suaccessuser (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_host', 'dest_ip', 'dest_port', 'event_code', 'host', 'time', 'user'] |
| edit_regex_field | host |  | ['\d\dZ\s+({dest_host}({host}[\w\-.]+))\s+su - su_ok', 'authHost=\"*({dest_host}({host}[^\"]+))\"'] |
| added_regex_field | dest_host |  | ['\d\dZ\s+({dest_host}({host}[\w\-.]+))\s+su - su_ok', 'authHost=\"*({dest_host}({host}[^\"]+))\"'] |
| removed_attribute | DupFields |  | N/A |
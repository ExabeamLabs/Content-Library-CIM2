# Code Changes for helpsystems-powertechiam-kv-endpoint-login-success-loginok (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'host', 'time', 'user'] |
| edit_regex_field | host |  | ['authHost=\"*({dest_host}({host}[^\"]+))\"'] |
| added_regex_field | dest_host |  | ['authHost=\"*({dest_host}({host}[^\"]+))\"'] |
| removed_attribute | DupFields |  | N/A |
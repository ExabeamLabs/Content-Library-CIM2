# Code Changes for microsoft-evsecurity-json-endpoint-lock-success-4800 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'time', 'user'] |
| edit_regex_field | host |  | ['"(Hostname|Computer)":"({dest_host}({host}[^"]+))'] |
| added_regex_field | dest_host |  | ['"(Hostname|Computer)":"({dest_host}({host}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |
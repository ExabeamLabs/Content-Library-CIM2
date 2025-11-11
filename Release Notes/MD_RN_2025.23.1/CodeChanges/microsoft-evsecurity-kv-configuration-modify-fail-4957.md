# Code Changes for microsoft-evsecurity-kv-configuration-modify-fail-4957 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'dest_user', 'domain', 'event_code', 'event_name', 'failure_reason', 'host', 'time', 'user', 'user_uid'] |
| edit_regex_field | host |  | ['dhost=({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['dhost=({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |
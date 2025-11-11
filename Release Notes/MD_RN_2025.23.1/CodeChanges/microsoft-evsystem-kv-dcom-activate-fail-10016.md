# Code Changes for microsoft-evsystem-kv-dcom-activate-fail-10016 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app_id', 'cls_id', 'dest_host', 'domain', 'event_code', 'failure_reason', 'host', 'operation', 'src_host', 'src_ip', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['ComputerName(:|=)\s*({dest_host}({host}[\w.-]+))'] |
| added_regex_field | dest_host |  | ['ComputerName(:|=)\s*({dest_host}({host}[\w.-]+))'] |
| removed_attribute | DupFields |  | N/A |
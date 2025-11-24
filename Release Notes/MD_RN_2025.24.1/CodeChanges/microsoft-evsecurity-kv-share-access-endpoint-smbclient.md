# Code Changes for microsoft-evsecurity-kv-share-access-endpoint-smbclient (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_ip', 'dest_port', 'event_code', 'event_name', 'host', 'log_name', 'result', 'session_id', 'src_host', 'time'] |
| edit_regex_field | host |  | ['({src_host}({host}[\w\-\.]+))\s+None'] |
| added_regex_field | src_host |  | ['({src_host}({host}[\w\-\.]+))\s+None'] |
| removed_attribute | DupFields |  | N/A |
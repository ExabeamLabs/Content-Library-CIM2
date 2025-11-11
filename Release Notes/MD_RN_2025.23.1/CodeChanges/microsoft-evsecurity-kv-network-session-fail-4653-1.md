# Code Changes for microsoft-evsecurity-kv-network-session-fail-4653-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_method', 'dest_host', 'dest_ip', 'dest_port', 'event_code', 'event_name', 'failure_reason', 'host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | host |  | [':\d+\s({dest_host}({host}[^\s]+))\sMSWinEventLog'] |
| added_regex_field | dest_host |  | [':\d+\s({dest_host}({host}[^\s]+))\sMSWinEventLog'] |
| removed_attribute | DupFields |  | N/A |
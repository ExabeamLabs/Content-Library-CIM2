# Code Changes for microsoft-evsecurity-cef-network-session-fail-4653 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'dest_host', 'dest_ip', 'dest_port', 'event_code', 'event_id', 'event_name', 'failure_reason', 'host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | host |  | ['"computer":"({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['"computer":"({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |
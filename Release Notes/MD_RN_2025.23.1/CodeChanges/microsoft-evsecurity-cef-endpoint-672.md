# Code Changes for microsoft-evsecurity-cef-endpoint-672 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'result_code', 'time', 'user'] |
| edit_regex_field | host |  | ['\sdvchost=({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['\sdvchost=({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |
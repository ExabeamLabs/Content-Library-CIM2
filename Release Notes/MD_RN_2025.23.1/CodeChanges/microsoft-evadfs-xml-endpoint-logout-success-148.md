# Code Changes for microsoft-evadfs-xml-endpoint-logout-success-148 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'channel', 'dest_host', 'event_code', 'host', 'run_level', 'time'] |
| edit_regex_field | host |  | ['<Computer>({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['<Computer>({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |
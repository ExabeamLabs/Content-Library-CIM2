# Code Changes for microsoft-evsecurity-xml-endpoint-logout-success-4779 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'result', 'run_level', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['<Computer>({dest_host}({host}[\w\-.]+))', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({dest_host}({host}[\w_\-\.]+))'] |
| added_regex_field | dest_host |  | ['<Computer>({dest_host}({host}[\w\-.]+))', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({dest_host}({host}[\w_\-\.]+))'] |
| removed_attribute | DupFields |  | N/A |
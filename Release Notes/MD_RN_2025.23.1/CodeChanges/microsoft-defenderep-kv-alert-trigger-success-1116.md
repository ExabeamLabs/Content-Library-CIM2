# Code Changes for microsoft-defenderep-kv-alert-trigger-success-1116 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_severity', 'alert_type', 'domain', 'event_code', 'host', 'src_host', 'threat_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['<Computer>({src_host}({host}[^<]+))<\/Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({src_host}({host}[\w_\-\.]+))'] |
| added_regex_field | src_host |  | ['<Computer>({src_host}({host}[^<]+))<\/Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({src_host}({host}[\w_\-\.]+))'] |
| removed_attribute | DupFields |  | N/A |
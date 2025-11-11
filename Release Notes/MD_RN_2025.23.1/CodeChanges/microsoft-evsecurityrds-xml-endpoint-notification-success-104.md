# Code Changes for microsoft-evsecurityrds-xml-endpoint-notification-success-104 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['<Computer>({src_host}({host}[\w\-.]+))', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({src_host}({host}[\w_\-\.]+))'] |
| edit_regex_field | src_host |  | ['<Computer>(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w\-\.]+))', '<Computer>({src_host}({host}[\w\-.]+))', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({src_host}({host}[\w_\-\.]+))'] |
| removed_attribute | DupFields |  | N/A |
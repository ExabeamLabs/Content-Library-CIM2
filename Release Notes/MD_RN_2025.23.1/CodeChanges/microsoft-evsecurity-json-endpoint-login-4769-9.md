# Code Changes for microsoft-evsecurity-json-endpoint-login-4769-9 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | computer_name |  | ['ComputerName=({host}({computer_name}[\w.\-]+))'] |
| edit_regex_field | host |  | ['(?!\d+)({host}[\w\-.]+),([^,]*,)?Kerberos サービス チケットが要求されました。', 'ComputerName=({host}({computer_name}[\w.\-]+))'] |
| removed_attribute | DupFields |  | N/A |
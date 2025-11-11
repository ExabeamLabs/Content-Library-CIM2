# Code Changes for microsoft-evsecurity-csv-endpoint-login-success-4770 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | computer_name |  | ['ComputerName=({host}({computer_name}[\w.\-]+))'] |
| edit_regex_field | host |  | ['(?!\d+)({host}[\w\-.]+),([^,]*,)?Kerberos サービス チケットが更新されました。', 'ComputerName=({host}({computer_name}[\w.\-]+))'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for microsoft-evsecurity-csv-endpoint-login-4768 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | computer_name |  | ['ComputerName=({host}({computer_name}[\w.\-]+))'] |
| edit_regex_field | host |  | ['({host}(?!\d+)[\w\-.]+),([^,]*,)?Kerberos 認証チケット \(TGT\) が要求されました。', 'ComputerName=({host}({computer_name}[\w.\-]+))'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for microsoft-evsecurity-csv-user-password-reset-success-4724-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['computer_name', 'dest_domain', 'dest_host', 'dest_user', 'domain', 'event_code', 'host', 'login_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['(?!\d+)({host}[\w\-.]+),([^,]*,)?アカウントのパスワードのリセットが試行されました。', 'ComputerName=({host}[\w.\-]+)'] |
| added_regex_field | dest_host |  | ['ComputerName=({dest_host}[\w.\-]+)'] |
| removed_attribute | DupFields |  | N/A |
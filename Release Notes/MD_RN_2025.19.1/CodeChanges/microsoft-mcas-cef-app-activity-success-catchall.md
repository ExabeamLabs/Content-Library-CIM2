# Code Changes for microsoft-mcas-cef-app-activity-success-catchall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'action', 'additional_info', 'app', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'file_type', 'file_url', 'group_name', 'host', 'object', 'operation', 'policy_name', 'rule_action', 'time', 'user', 'user_agent'] |
| edit_regex_field | action |  | ['\WSecurity event:\s*({action}[^\s]+)\s', '\Wmsg=\s*({action}Trash)\s({file_type}[^:]+):', '\Wmsg=\s*({action}[^\s]+)\sa company ({file_type}[^:]+):', '\Wmsg=\s*({action}[^\s]+)\sowner to group: user.+?\sto group\s({group_name}.+?)\ssuser='] |
| added_regex_field | file_type |  | ['\Wmsg=\s*({action}Trash)\s({file_type}[^:]+):', '\Wmsg=\s*({action}[^\s]+)\sa company ({file_type}[^:]+):'] |
| added_regex_field | group_name |  | ['\Wmsg=\s*({action}[^\s]+)\sowner to group: user.+?\sto group\s({group_name}.+?)\ssuser='] |
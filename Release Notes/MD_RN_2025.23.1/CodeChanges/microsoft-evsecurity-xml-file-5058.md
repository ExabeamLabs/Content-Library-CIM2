# Code Changes for microsoft-evsecurity-xml-file-5058 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'activity_id', 'channel', 'dest_host', 'dest_user_sid', 'domain', 'error_code', 'event_code', 'event_id', 'event_name', 'failure_reason', 'file_dir', 'file_ext', 'file_name', 'file_path', 'group_domain', 'group_id', 'group_name', 'host', 'key_name', 'key_type', 'login_id', 'operation', 'process_id', 'provider_name', 'result', 'return_code', 'rule', 'rule_id', 'run_level', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['<Computer>({dest_host}({host}[\w\.\-]+))<', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({dest_host}({host}[\w_\-\.]+))'] |
| added_regex_field | dest_host |  | ['<Computer>({dest_host}({host}[\w\.\-]+))<', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({dest_host}({host}[\w_\-\.]+))'] |
| removed_attribute | DupFields |  | N/A |
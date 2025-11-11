# Code Changes for microsoft-evsecurity-json-endpoint-unlock-success-4801 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'activity_id', 'app', 'dest_domain', 'dest_host', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'login_type', 'os', 'privileges', 'process_id', 'provider_name', 'result', 'sid_history', 'src_host', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['"hostname"+:"+({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['"hostname"+:"+({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |
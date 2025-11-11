# Code Changes for microsoft-evsecurity-json-endpoint-notification-4611 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_id', 'additional_info', 'category', 'event_code', 'event_name', 'host', 'log_source', 'login_id', 'process_id', 'process_name', 'result', 'src_user', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | user |  | ['"SubjectUserName"+:"+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | src_user |  | ['"SubjectUserName"+:"+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| removed_attribute | DupFields |  | N/A |
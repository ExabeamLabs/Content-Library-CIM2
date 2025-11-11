# Code Changes for microsoft-evsecurity-json-ds-object-activity-success-4662-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'action', 'activity_id', 'additional_info', 'app', 'dest_domain', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'login_type', 'object', 'object_name', 'object_server', 'object_type', 'operation', 'os', 'privileges', 'process_id', 'provider_name', 'result', 'sid_history', 'src_domain', 'src_host', 'src_user', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | object_name |  | ['"ObjectName":"({object}({object_name}[^"]+))"'] |
| edit_regex_field | src_domain |  | ['"+SubjectDomainName"+:"+({domain}({src_domain}[^"]+))'] |
| edit_regex_field | src_user |  | ['"+SubjectUserName"+:"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user |  | ['"+SubjectUserName"+:"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', '"user"+:"+(SYSTEM|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | domain |  | ['"+SubjectDomainName"+:"+({domain}({src_domain}[^"]+))'] |
| added_regex_field | object |  | ['"ObjectName":"({object}({object_name}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |
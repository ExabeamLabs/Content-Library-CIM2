# Code Changes for unix-auditd-kv-user-switch-success-sessionopen (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'account_id', 'dest_host', 'dest_user', 'email_address', 'host', 'host_ip', 'login_type_text', 'result', 'session_id', 'time', 'user', 'user_id'] |
| added_regex_field | login_type_text |  | ['\sterminal=(\?|({login_type_text}[^=]+?))\s+\w+='] |
| added_regex_field | result |  | ['\sres=({result}\w+)'] |
| edit_attribute | activity_type |  | ['endpoint-login:success', 'scheduled_task-start:fail', 'scheduled_task-start:success', 'user-switch:success'] |
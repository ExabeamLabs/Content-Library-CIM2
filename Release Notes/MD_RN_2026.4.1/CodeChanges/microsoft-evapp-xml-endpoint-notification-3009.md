# Code Changes for microsoft-evapp-xml-endpoint-notification-3009 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_id', 'channel', 'domain', 'event_code', 'event_id', 'event_name', 'failure_reason', 'file_path', 'group_domain', 'group_id', 'group_name', 'host', 'key_name', 'key_type', 'login_id', 'operation', 'process_id', 'provider_name', 'result', 'return_code', 'rule', 'rule_id', 'run_level', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |
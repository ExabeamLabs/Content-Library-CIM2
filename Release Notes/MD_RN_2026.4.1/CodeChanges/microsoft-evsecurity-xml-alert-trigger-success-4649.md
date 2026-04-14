# Code Changes for microsoft-evsecurity-xml-alert-trigger-success-4649 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_id', 'additional_info', 'alert_name', 'alert_type', 'auth_process', 'channel', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'process_id', 'provider_name', 'result', 'run_level', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |
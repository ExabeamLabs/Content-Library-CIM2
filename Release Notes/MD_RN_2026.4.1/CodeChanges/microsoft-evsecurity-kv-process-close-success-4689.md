# Code Changes for microsoft-evsecurity-kv-process-close-success-4689 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'action', 'channel', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'operation', 'process_id', 'process_name', 'process_path', 'provider_name', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['\schannel="+({channel}[^"]+)"'] |
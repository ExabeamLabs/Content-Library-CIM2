# Code Changes for microsoft-evsecurity-kv-user-privilege-modify-success-4703 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'channel', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'operation', 'privileges', 'process_id', 'process_path', 'provider_name', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['\schannel="+({channel}[^"]+)"'] |
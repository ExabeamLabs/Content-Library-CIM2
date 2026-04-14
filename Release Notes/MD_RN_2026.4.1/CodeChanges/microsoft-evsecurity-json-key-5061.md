# Code Changes for microsoft-evsecurity-json-key-5061 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_name', 'host', 'key_name', 'login_id', 'process_id', 'provider_name', 'severity', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |
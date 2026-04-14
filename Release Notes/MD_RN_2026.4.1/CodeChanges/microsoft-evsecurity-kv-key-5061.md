# Code Changes for microsoft-evsecurity-kv-key-5061 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_name', 'file_path', 'host', 'key_name', 'key_type', 'login_id', 'operation', 'provider_name', 'result', 'return_code', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['Channel"?(:|>)"?({channel}[^"<]+)'] |
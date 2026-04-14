# Code Changes for microsoft-evsecurity-kv-endpoint-lock-success-4800-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'time', 'user'] |
| added_regex_field | channel |  | ['"channel":"({channel}[^"]+)"'] |
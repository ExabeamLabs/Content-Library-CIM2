# Code Changes for microsoft-evpowershell-json-process-create-success-4104 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_name', 'host', 'process_id', 'process_name', 'scriptblock_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |
# Code Changes for microsoft-evpowershell-json-script-execute-success-4104 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_name', 'host', 'process_id', 'process_name', 'scriptblock_id', 'scriptblock_text', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |
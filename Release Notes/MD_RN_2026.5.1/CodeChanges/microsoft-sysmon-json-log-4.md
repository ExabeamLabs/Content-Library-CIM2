# Code Changes for microsoft-sysmon-json-log-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'log_name', 'process_id', 'result', 'service_state', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel"+:"+({channel}[^"]+)"'] |
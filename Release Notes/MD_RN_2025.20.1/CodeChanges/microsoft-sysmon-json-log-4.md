# Code Changes for microsoft-sysmon-json-log-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_id', 'event_name', 'host', 'log_name', 'process_id', 'result', 'service_state', 'time', 'user', 'user_sid'] |
| removed_regex_field | state |  | [] |
| added_regex_field | service_state |  | ['State":"({service_state}[^"]+)'] |
# Code Changes for microsoft-sysmon-xml-service-state-modify-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_code', 'event_id', 'event_name', 'host', 'log_name', 'result', 'run_level', 'service_state', 'time', 'user_sid'] |
| removed_regex_field | state |  | [] |
| added_regex_field | service_state |  | ['<Data Name\\*=(\'|")State(\'|")>({service_state}.+?)<\/Data>'] |
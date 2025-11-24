# Code Changes for tenable-tie-str-app-notification-success-tenablead (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'app', 'domain', 'event_code', 'event_name', 'host', 'operation', 'os', 'os_version', 'process_id', 'result', 'time'] |
| edit_regex_field | event_name |  | ['Tenable\.ad\s*\[\S+\]:\s("[^"]*"\s){2}"({operation}({event_name}[^"]+))"'] |
| added_regex_field | operation |  | ['Tenable\.ad\s*\[\S+\]:\s("[^"]*"\s){2}"({operation}({event_name}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |
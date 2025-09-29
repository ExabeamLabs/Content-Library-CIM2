# Code Changes for infoblox-nios-kv-app-notification-failure (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_category', 'host', 'operation', 'status_msg', 'time'] |
| removed_regex_field | state |  | [] |
| added_regex_field | status_msg |  | ['State: ({status_msg}[^,\s]+)'] |
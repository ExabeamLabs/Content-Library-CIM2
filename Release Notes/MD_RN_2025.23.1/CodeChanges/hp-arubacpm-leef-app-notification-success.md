# Code Changes for hp-arubacpm-leef-app-notification-success (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'event_name', 'host', 'operation', 'src_ip', 'time'] |
| added_regex_field | event_name |  | ['description=({event_name}[^=]+?)\.'] |
| removed_attribute | DupFields |  | N/A |
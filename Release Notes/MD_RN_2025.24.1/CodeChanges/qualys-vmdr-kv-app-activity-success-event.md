# Code Changes for qualys-vmdr-kv-app-activity-success-event (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'category', 'event_name', 'operation', 'process_id', 'process_name', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | event_name |  | ["\sEVENT='({operation}({event_name}[^']+))"] |
| added_regex_field | operation |  | ["\sEVENT='({operation}({event_name}[^']+))"] |
| removed_attribute | DupFields |  | N/A |
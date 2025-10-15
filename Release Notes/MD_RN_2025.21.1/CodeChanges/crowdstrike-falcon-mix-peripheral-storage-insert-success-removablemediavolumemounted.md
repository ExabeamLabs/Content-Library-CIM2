# Code Changes for crowdstrike-falcon-mix-peripheral-storage-insert-success-removablemediavolumemounted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['aid', 'cid', 'device_class', 'device_id', 'device_pid', 'device_vid', 'event_code', 'host', 'operation', 'os', 'time', 'user'] |
| edit_regex_field | event_code |  | ['"event_simpleName":"({operation}({event_code}[^"]+))'] |
| added_regex_field | operation |  | ['"event_simpleName":"({operation}({event_code}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |
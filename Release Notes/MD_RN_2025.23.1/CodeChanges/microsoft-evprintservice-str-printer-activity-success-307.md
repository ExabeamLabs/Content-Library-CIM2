# Code Changes for microsoft-evprintservice-str-printer-activity-success-307 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'activity_2', 'bytes', 'dest_host', 'dest_ip', 'dest_port', 'event_code', 'event_name', 'host', 'num_pages', 'object', 'operation', 'printer_name', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | event_name |  | ['({operation}({event_name}Printing a document))'] |
| added_regex_field | operation |  | ['({operation}({event_name}Printing a document))'] |
| removed_attribute | DupFields |  | N/A |
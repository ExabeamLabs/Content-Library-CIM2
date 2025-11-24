# Code Changes for xps-s-kv-printer-activity-success-set (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes', 'dest_host', 'object', 'operation', 'printer_name'] |
| edit_regex_field | printer_name |  | ['printer=({dest_host}({printer_name}[^\s]+))'] |
| added_regex_field | dest_host |  | ['printer=({dest_host}({printer_name}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |
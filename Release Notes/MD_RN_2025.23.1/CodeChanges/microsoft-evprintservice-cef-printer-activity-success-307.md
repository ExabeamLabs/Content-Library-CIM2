# Code Changes for microsoft-evprintservice-cef-printer-activity-success-307 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'host', 'num_pages', 'object', 'operation', 'printer_id', 'printer_name', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['\sdvchost=({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['\sdvchost=({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for dg-ep-kv-printer-activity-success-22 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'host', 'object', 'printer_name', 'src_host', 'time', 'user'] |
| edit_regex_field | host |  | ['Computer_Name="([^\/"\\]+(\/|\\))?({src_host}({host}[\w\-\.]+))"'] |
| added_regex_field | src_host |  | ['Computer_Name="([^\/"\\]+(\/|\\))?({src_host}({host}[\w\-\.]+))"'] |
| removed_attribute | DupFields |  | N/A |
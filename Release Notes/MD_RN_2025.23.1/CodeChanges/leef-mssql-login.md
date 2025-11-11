# Code Changes for leef-mssql-login (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'dest_host', 'domain', 'event_code', 'host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['resource=({dest_host}({host}[\w\-.]+?))\s*\w+='] |
| added_regex_field | dest_host |  | ['resource=({dest_host}({host}[\w\-.]+?))\s*\w+='] |
| removed_attribute | DupFields |  | N/A |
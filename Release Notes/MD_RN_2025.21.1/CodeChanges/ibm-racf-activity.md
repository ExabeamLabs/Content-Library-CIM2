# Code Changes for ibm-racf-activity (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'db_object', 'db_operation', 'db_query', 'db_user', 'event_name', 'full_name', 'host', 'src_ip', 'src_port', 'user'] |
| edit_regex_field | event_name |  | ['EVNTNAME=({db_operation}({event_name}[^=]+?))\s\w+='] |
| added_regex_field | db_operation |  | ['EVNTNAME=({db_operation}({event_name}[^=]+?))\s\w+='] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for beyondtrust-pi-app-activity (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'account_domain', 'additional_info', 'app', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'operation', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | operation |  | ['\ssEventID=\\?"({event_name}({operation}[^"]+?))\\?"'] |
| added_regex_field | event_name |  | ['\ssEventID=\\?"({event_name}({operation}[^"]+?))\\?"'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for pingidentity-pi-cef-app-authentication-fail-failure-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'connection_id', 'email_address', 'event_name', 'host', 'operation', 'protocol', 'result', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | event_name |  | ['\|Ping Identity\|PingFederate\|([^\|]*){3}\|({operation}({event_name}[^\|]+))'] |
| added_regex_field | operation |  | ['\|Ping Identity\|PingFederate\|([^\|]*){3}\|({operation}({event_name}[^\|]+))'] |
| removed_attribute | DupFields |  | N/A |
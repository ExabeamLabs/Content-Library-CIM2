# Code Changes for symantec-wss-str-endpoint-login-fail-postponedloginauthentication (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'event_category', 'event_code', 'event_name', 'host', 'protocol', 'realm', 'severity', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | dest_host |  | ['({dest_host}[\w.-]+) ProxySG:'] |
| removed_attribute | DupFields |  | N/A |
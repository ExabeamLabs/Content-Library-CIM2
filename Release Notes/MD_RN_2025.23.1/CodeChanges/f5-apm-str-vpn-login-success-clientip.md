# Code Changes for f5-apm-str-vpn-login-success-clientip (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_port', 'host', 'session_id', 'src_ip'] |
| edit_regex_field | dest_port |  | ['Listener \/Common\/({dest_host}({host}[\w\-\.]+))_({dest_port}\d{1,5})\s'] |
| edit_regex_field | host |  | ['Listener \/Common\/({dest_host}({host}[\w\-\.]+))_({dest_port}\d{1,5})\s'] |
| added_regex_field | dest_host |  | ['Listener \/Common\/({dest_host}({host}[\w\-\.]+))_({dest_port}\d{1,5})\s'] |
| removed_attribute | DupFields |  | N/A |
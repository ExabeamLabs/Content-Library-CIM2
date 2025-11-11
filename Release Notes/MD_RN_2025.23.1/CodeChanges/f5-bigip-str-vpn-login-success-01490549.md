# Code Changes for f5-bigip-str-vpn-login-success-01490549 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access_group', 'dest_host', 'host', 'session_id', 'src_ip', 'src_port', 'src_translated_ip', 'time'] |
| edit_regex_field | host |  | ['(\s|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s({dest_host}({host}[\w\-.]+))\s', '\d\d:\d\d\s+({dest_host}({host}[\w\-.]+))\s([^\s]+\s)?[^\s]+\[\d+\]'] |
| edit_regex_field | time |  | ['(\s|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s({dest_host}({host}[\w\-.]+))\s'] |
| added_regex_field | dest_host |  | ['(\s|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s({dest_host}({host}[\w\-.]+))\s', '\d\d:\d\d\s+({dest_host}({host}[\w\-.]+))\s([^\s]+\s)?[^\s]+\[\d+\]'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for cyberark-pam-mix-app-login-success-logon (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'app', 'dest_host', 'domain', 'email_address', 'event_code', 'event_subtype', 'gateway_station', 'host', 'operation', 'result_reason', 'safe_value', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)', '({time}\w+\s+\d\d\s+\d\d:\d\d:\d\d)\s*({dest_host}[\w\-.]+)\s*LEEF', '({time}\w+\s+\d\d\s+\d\d:\d\d:\d\d)\s*({host}[\w\-.]+)\s*LEEF'] |
| added_regex_field | dest_host |  | ['(\d\d:\d\d:\d\d|\d\d\d\d-\d\d-\d\d\w\d\d:\d\d:\d\d\w) ({dest_host}[\w\-.]+) (LEEF|CEF)', '({time}\w+\s+\d\d\s+\d\d:\d\d:\d\d)\s*({dest_host}[\w\-.]+)\s*LEEF'] |
| removed_attribute | DupFields |  | N/A |
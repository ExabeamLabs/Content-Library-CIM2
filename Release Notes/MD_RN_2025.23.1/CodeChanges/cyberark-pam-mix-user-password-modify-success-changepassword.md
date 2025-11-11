# Code Changes for cyberark-pam-mix-user-password-modify-success-changepassword (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'action', 'dest_host', 'domain', 'email_address', 'event_code', 'gateway_station', 'host', 'result_reason', 'safe_value', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['({time}(\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ|\w+\s+\d\d\s+\d\d:\d\d:\d\d))\s*({dest_host}({host}[\w\-.]+))\s*LEEF', '({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) ({dest_host}({host}[\w\-.]+)) (LEEF|CEF)'] |
| edit_regex_field | time |  | ['({time}(\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ|\w+\s+\d\d\s+\d\d:\d\d:\d\d))\s*({dest_host}({host}[\w\-.]+))\s*LEEF', '({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) ({dest_host}({host}[\w\-.]+)) (LEEF|CEF)'] |
| added_regex_field | dest_host |  | ['({time}(\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ|\w+\s+\d\d\s+\d\d:\d\d:\d\d))\s*({dest_host}({host}[\w\-.]+))\s*LEEF', '({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) ({dest_host}({host}[\w\-.]+)) (LEEF|CEF)'] |
| removed_attribute | DupFields |  | N/A |
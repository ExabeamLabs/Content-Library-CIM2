# Code Changes for hp-hpilo-str-app-login-success-browserlogin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'dest_host', 'event_name', 'host', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | dest_host |  | ['\d\d:\d\d:\d\dZ\s({dest_host}[^\s]+)\s\#ILO'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for unix-unix-str-endpoint-login-success-startedsession (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'email_address', 'event_code', 'host', 'user'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w\-.]+))\s+systemd: Started Session'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w\-.]+))\s+systemd: Started Session'] |
| removed_attribute | DupFields |  | N/A |
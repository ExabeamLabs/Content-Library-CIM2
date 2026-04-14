# Code Changes for unix-unix-json-user-switch-success-session (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ["yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"] |
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'dest_user', 'dest_user_id', 'event_code', 'host', 'process_id', 'time', 'user_id'] |
| edit_regex_field | dest_user |  | ['({additional_info}session (opened|closed) for user\s*({dest_user}[^\s"]+))("|$|\s*by\s*(\(uid=({dest_user_id}\d+)\))?)', 'exa_regex=({additional_info}session (opened|closed) for user\s*({dest_user}[^\s"]+))("|$|\s*by\s*(\(uid=({dest_user_id}\d+)\))?)'] |
| edit_regex_field | dest_user_id |  | ['({additional_info}session (opened|closed) for user\s*({dest_user}[^\s"]+))("|$|\s*by\s*(\(uid=({dest_user_id}\d+)\))?)', 'exa_regex=({additional_info}session (opened|closed) for user\s*({dest_user}[^\s"]+))("|$|\s*by\s*(\(uid=({dest_user_id}\d+)\))?)'] |
| edit_regex_field | process_id |  | ['exa_regex="pid":"({process_id}\d+)', 'exa_regex="pid":"({process_id}\d+)'] |
| added_regex_field | additional_info |  | ['({additional_info}session (opened|closed) for user\s*({dest_user}[^\s"]+))("|$|\s*by\s*(\(uid=({dest_user_id}\d+)\))?)', 'exa_regex=({additional_info}session (opened|closed) for user\s*({dest_user}[^\s"]+))("|$|\s*by\s*(\(uid=({dest_user_id}\d+)\))?)'] |
| added_regex_field | dest_host |  | ['"host":"({host}({dest_host}[^"]+))'] |
| added_regex_field | event_code |  | ['"ident":"({event_code}[^"]+)'] |
| added_regex_field | host |  | ['"host":"({host}({dest_host}[^"]+))'] |
| added_regex_field | time |  | ['"timestamp":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\dZ)'] |
| edit_attribute | activity_type |  | ['endpoint-login:success', 'process-close:success', 'process-open:success', 'user-switch:success'] |
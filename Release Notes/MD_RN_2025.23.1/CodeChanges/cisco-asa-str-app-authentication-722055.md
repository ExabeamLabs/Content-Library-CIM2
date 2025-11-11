# Code Changes for cisco-asa-str-app-authentication-722055 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'email_address', 'event_code', 'event_name', 'group_name', 'host', 'os', 'priority', 'realm', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| added_regex_field | realm |  | ['Group <({realm}[^>]+)>'] |
| removed_attribute | DupFields |  | N/A |
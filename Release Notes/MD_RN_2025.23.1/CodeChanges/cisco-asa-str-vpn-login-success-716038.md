# Code Changes for cisco-asa-str-vpn-login-success-716038 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['email_address', 'event_code', 'group_name', 'priority', 'realm', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | realm |  | ['Group\s*<({realm}.*?)>'] |
| removed_attribute | DupFields |  | N/A |
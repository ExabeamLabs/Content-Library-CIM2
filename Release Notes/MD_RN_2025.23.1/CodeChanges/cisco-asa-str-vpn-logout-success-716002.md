# Code Changes for cisco-asa-str-vpn-logout-success-716002 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'domain', 'email_address', 'event_code', 'group_name', 'host', 'priority', 'realm', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | realm |  | ['Group\s*<({realm}.*?)>'] |
| removed_attribute | DupFields |  | N/A |
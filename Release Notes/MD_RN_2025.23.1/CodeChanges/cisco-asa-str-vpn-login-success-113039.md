# Code Changes for cisco-asa-str-vpn-login-success-113039 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'domain', 'email_address', 'event_code', 'group_name', 'host', 'priority', 'realm', 'src_host', 'src_ip', 'time', 'user'] |
| added_regex_field | account |  | ['\sUser\s*<({account}[\w\.\-\!\#\^\~]{1,40}\$?)>'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for securenet-s-kv-vpn-success-pppd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'event_code', 'event_name', 'host', 'src_ip', 'src_port', 'src_translated_ip', 'time', 'user'] |
| edit_regex_field | user |  | ['\Wusername="({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | account |  | ['\Wusername="({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| removed_attribute | DupFields |  | N/A |
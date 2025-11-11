# Code Changes for cisco-dhcp-kv-endpoint-login-success-domain (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'time', 'user'] |
| added_regex_field | user |  | ['\shn="({user}[\w\.\-\!\#\^\~]{1,40}\$?)"'] |
| removed_attribute | DupFields |  | N/A |
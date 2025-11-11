# Code Changes for cisco-ise-kv-vpn-login-success-attempts (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'auth_server', 'badge_id', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'failure_reason', 'os', 'os_version', 'realm', 'session_id', 'src_ip', 'src_port', 'src_translated_ip', 'time', 'user'] |
| edit_regex_field | domain |  | [',\s*User-Name=(({domain}[^\s\\\/]+)(\/+|\\+))?(?:(\w{2}\-){5}\w{2}|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user |  | [',\s*User-Name=(({domain}[^\s\\\/]+)(\/+|\\+))?(?:(\w{2}\-){5}\w{2}|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | account |  | [',\s*User-Name=(({domain}[^\s\\\/]+)(\/+|\\+))?(?:(\w{2}\-){5}\w{2}|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for forcepoint-wsg-cef-http-session-security (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'bytes_in', 'bytes_out', 'category', 'category_id', 'dest_ip', 'dest_port', 'first_name', 'full_name', 'host', 'last_name', 'method', 'mime', 'orig_user', 'protocol', 'src_ip', 'src_port', 'time', 'uri_path', 'uri_query', 'url', 'user', 'user_agent', 'user_ou', 'web_domain'] |
| edit_regex_field | user |  | ['\ssuser=(-|(?!LDAP:)({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s\w+='] |
| added_regex_field | orig_user |  | ['\ssuser=(-|(?!LDAP:)({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s\w+='] |
| removed_attribute | DupFields |  | N/A |
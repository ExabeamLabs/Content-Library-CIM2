# Code Changes for symantec-wss-cef-http-session-proxysg (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'bytes_in', 'bytes_out', 'category', 'dest_ip', 'dest_port', 'email_address', 'host', 'http_response_code', 'method', 'mime', 'orig_user', 'protocol', 'proxy_action', 'referrer', 'src_host', 'src_ip', 'src_port', 'time', 'uri_path', 'uri_query', 'url', 'user', 'user_agent', 'web_domain'] |
| edit_regex_field | email_address |  | ['\ssuser=(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s\w+='] |
| edit_regex_field | user |  | ['\ssuser=(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s\w+='] |
| added_regex_field | orig_user |  | ['\ssuser=(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s\w+='] |
| removed_attribute | DupFields |  | N/A |
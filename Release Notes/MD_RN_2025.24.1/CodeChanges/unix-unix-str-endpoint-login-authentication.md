# Code Changes for unix-unix-str-endpoint-login-authentication (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'auth_method', 'dest_host', 'dest_ip', 'dest_port', 'dest_user', 'domain', 'event_code', 'failure_reason', 'host', 'process_id', 'process_name', 'result', 'time', 'user'] |
| edit_regex_field | account |  | ['\saccount:\s*<(({domain}[^\\\s>]+)\\+)?({dest_user}({account}[^\\\s>]+))>'] |
| edit_regex_field | domain |  | ['\saccount:\s*<(({domain}[^\\\s>]+)\\+)?({dest_user}({account}[^\\\s>]+))>'] |
| added_regex_field | dest_user |  | ['\saccount:\s*<(({domain}[^\\\s>]+)\\+)?({dest_user}({account}[^\\\s>]+))>'] |
| removed_attribute | DupFields |  | N/A |
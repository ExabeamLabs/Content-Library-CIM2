# Code Changes for unix-unix-str-endpoint-logout-disconnected (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | src_port |  | [' Disconnected from( authenticating user \S+)? (::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', '\s+port\s+({src_port}\d+)'] |
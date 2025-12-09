# Code Changes for passwordmngrpro-p-str-user-switch-success-pwdretrieved (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_ip', 'dest_port', 'dest_user', 'first_name', 'host', 'last_name', 'safe_value', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | dest_user |  | ['\sSuccess\s[^\s]+\s+({safe_value}[^:]+):({account}({dest_user}[^:]+)):'] |
| edit_regex_field | safe_value |  | ['\sSuccess\s[^\s]+\s+({safe_value}[^:]+):({account}({dest_user}[^:]+)):'] |
| added_regex_field | account |  | ['\sSuccess\s[^\s]+\s+({safe_value}[^:]+):({account}({dest_user}[^:]+)):'] |
| removed_attribute | DupFields |  | N/A |
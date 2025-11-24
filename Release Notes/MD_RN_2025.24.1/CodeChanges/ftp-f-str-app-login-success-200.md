# Code Changes for ftp-f-str-app-login-success-200 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'host', 'result', 'src_ip', 'time', 'user'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w\.-]+))\s+(\S+\s+){2}\[\d+\]'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w\.-]+))\s+(\S+\s+){2}\[\d+\]'] |
| removed_attribute | DupFields |  | N/A |
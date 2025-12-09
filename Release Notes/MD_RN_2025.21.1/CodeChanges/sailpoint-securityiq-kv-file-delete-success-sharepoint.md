# Code Changes for sailpoint-securityiq-kv-file-delete-success-sharepoint (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'app', 'dest_ip', 'dest_port', 'domain', 'file_dir', 'file_ext', 'file_name', 'host', 'operation', 'time', 'user', 'user_sid'] |
| edit_regex_field | operation |  | ['actiontype\s:\s({access}({operation}[^\ ]+))(\s|\s\([^\)]+\)\s)\|'] |
| added_regex_field | access |  | ['actiontype\s:\s({access}({operation}[^\ ]+))(\s|\s\([^\)]+\)\s)\|'] |
| removed_attribute | DupFields |  | N/A |
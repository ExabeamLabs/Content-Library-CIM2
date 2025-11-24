# Code Changes for unix-auditbeat-json-file-create-success-file (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'action', 'bytes', 'file_path', 'host', 'time', 'user'] |
| edit_regex_field | action |  | ['"action":\["({access}({action}[^"]+))"'] |
| added_regex_field | access |  | ['"action":\["({access}({action}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for unix-unix-str-user-password-modify-fail-keyringpassword (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'failure_reason', 'host', 'host_ip', 'time'] |
| edit_regex_field | host |  | ['({time}\w+\s*\d+ \d\d:\d\d:\d\d)?\s*({host}[\w.\-]+)\s+passwd(:|\[)', '\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?'] |
| added_regex_field | time |  | ['({time}\w+\s*\d+ \d\d:\d\d:\d\d)?\s*({host}[\w.\-]+)\s+passwd(:|\[)'] |
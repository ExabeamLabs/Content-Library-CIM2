# Code Changes for unix-auditd-kv-user-switch-success-userrolechange (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | ['<\d+>\S+\s\d+\s\d{2}:\d{2}:\d{2}\s({dest_host}({host}[\w\-.]+))?\s?audispd:', '\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({dest_host}({host}[\w.\-]+))))\s+(\d\S+|tag_audit_log|({=dest_host}({=host}[\w.\-]+))\s)?', 'node=({dest_host}[^\s\.]+)'] |
| edit_regex_field | host |  | ['<\d+>\S+\s\d+\s\d{2}:\d{2}:\d{2}\s({dest_host}({host}[\w\-.]+))?\s?audispd:', '\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({dest_host}({host}[\w.\-]+))))\s+(\d\S+|tag_audit_log|({=dest_host}({=host}[\w.\-]+))\s)?'] |
| edit_regex_field | host_ip |  | ['\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({dest_host}({host}[\w.\-]+))))\s+(\d\S+|tag_audit_log|({=dest_host}({=host}[\w.\-]+))\s)?'] |
| removed_attribute | DupFields |  | N/A |
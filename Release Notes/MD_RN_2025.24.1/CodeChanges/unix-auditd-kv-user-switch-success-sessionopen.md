# Code Changes for unix-auditd-kv-user-switch-success-sessionopen (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'account_id', 'dest_host', 'dest_user', 'email_address', 'host', 'host_ip', 'session_id', 'time', 'user', 'user_id'] |
| edit_regex_field | account |  | ['\sacct=\"({dest_user}({account}[^\"]+))\"'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d ({dest_host}({host}[\w\-.]+))\s*(tag_audit_log(:|\s*)|audisp-syslog\[)', '\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({dest_host}({host}[\w.\-]+))))\s+(\d\S+|tag_audit_log|({=dest_host}({=host}[\w.\-]+))\s)?'] |
| edit_regex_field | host_ip |  | ['\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({dest_host}({host}[\w.\-]+))))\s+(\d\S+|tag_audit_log|({=dest_host}({=host}[\w.\-]+))\s)?'] |
| added_regex_field | dest_host |  | ['\d\d:\d\d:\d\d ({dest_host}({host}[\w\-.]+))\s*(tag_audit_log(:|\s*)|audisp-syslog\[)', '\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({dest_host}({host}[\w.\-]+))))\s+(\d\S+|tag_audit_log|({=dest_host}({=host}[\w.\-]+))\s)?'] |
| added_regex_field | dest_user |  | ['\sacct=\"({dest_user}({account}[^\"]+))\"'] |
| removed_attribute | DupFields |  | N/A |
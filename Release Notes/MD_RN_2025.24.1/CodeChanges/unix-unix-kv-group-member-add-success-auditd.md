# Code Changes for unix-unix-kv-group-member-add-success-auditd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'account_name', 'dest_host', 'group_name', 'host', 'host_ip', 'session_id', 'time', 'user_id'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?', '\s*({dest_host}({host}[\w\-.]+))\saudisp-syslog'] |
| added_regex_field | dest_host |  | ['\s*({dest_host}({host}[\w\-.]+))\saudisp-syslog'] |
| removed_attribute | DupFields |  | N/A |
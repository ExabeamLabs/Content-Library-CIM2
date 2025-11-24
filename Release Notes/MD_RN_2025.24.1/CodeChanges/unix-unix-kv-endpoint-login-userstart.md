# Code Changes for unix-unix-kv-endpoint-login-userstart (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_process', 'dest_host', 'event_code', 'event_name', 'host', 'host_ip', 'login_type_text', 'result', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w\-\.]+))\saudispd', '\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({dest_host}({host}[\w.\-]+))))\s+(\d\S+|tag_audit_log|({=dest_host}({=host}[\w.\-]+))\s)?', 'node=({dest_host}({host}[\w\.-]+))\s'] |
| edit_regex_field | host_ip |  | ['\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({dest_host}({host}[\w.\-]+))))\s+(\d\S+|tag_audit_log|({=dest_host}({=host}[\w.\-]+))\s)?'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w\-\.]+))\saudispd', '\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({dest_host}({host}[\w.\-]+))))\s+(\d\S+|tag_audit_log|({=dest_host}({=host}[\w.\-]+))\s)?', 'node=({dest_host}({host}[\w\.-]+))\s'] |
| removed_attribute | DupFields |  | N/A |
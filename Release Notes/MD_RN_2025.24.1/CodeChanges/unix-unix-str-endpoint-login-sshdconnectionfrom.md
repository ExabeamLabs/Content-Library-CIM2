# Code Changes for unix-unix-str-endpoint-login-sshdconnectionfrom (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'dest_mac', 'host', 'host_ip', 'process_id', 'process_name', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | host |  | ['({time}\w+\s\d+\s\d+:\d+:\d\d(\dZ)?)\s({dest_host}({host}[\w\-\.]+))(\s\w+)?\s*sshd\[', '\d\d(\dZ)?\s({dest_host}({host}[\w\-\.]+))(\s\w+)?\s*sshd\[', '\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({dest_host}({host}[\w.\-]+))))\s+(\d\S+|tag_audit_log|({=dest_host}({=host}[\w.\-]+))\s)?'] |
| edit_regex_field | host_ip |  | ['\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({dest_host}({host}[\w.\-]+))))\s+(\d\S+|tag_audit_log|({=dest_host}({=host}[\w.\-]+))\s)?'] |
| edit_regex_field | time |  | ['({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)', '({time}\w+\s\d+\s\d+:\d+:\d\d(\dZ)?)\s({dest_host}({host}[\w\-\.]+))(\s\w+)?\s*sshd\['] |
| added_regex_field | dest_host |  | ['({time}\w+\s\d+\s\d+:\d+:\d\d(\dZ)?)\s({dest_host}({host}[\w\-\.]+))(\s\w+)?\s*sshd\[', '\d\d(\dZ)?\s({dest_host}({host}[\w\-\.]+))(\s\w+)?\s*sshd\[', '\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({dest_host}({host}[\w.\-]+))))\s+(\d\S+|tag_audit_log|({=dest_host}({=host}[\w.\-]+))\s)?'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for unix-unixauditd-kv-endpoint-authentication-success-cryptokeyuser (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'additional_info', 'dest_host', 'dest_ip', 'dest_port', 'event_name', 'host', 'host_ip', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'session_id', 'src_host', 'src_ip', 'src_port', 'time', 'user_id'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w\-\.]+))\saudispd', '\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?', '\snode=({dest_host}({host}[\w\.-]+))\s'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w\-\.]+))\saudispd', '\snode=({dest_host}({host}[\w\.-]+))\s'] |
| removed_attribute | DupFields |  | N/A |
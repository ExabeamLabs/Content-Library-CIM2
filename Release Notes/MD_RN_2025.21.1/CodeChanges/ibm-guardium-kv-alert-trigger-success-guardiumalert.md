# Code Changes for ibm-guardium-kv-alert-trigger-success-guardiumalert (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'db_user', 'dest_ip', 'dest_port', 'host', 'process_dir', 'process_name', 'process_path', 'server_group', 'service_name', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | db_user |  | ['db-user=([^\\\^]+\\)?({account}({db_user}[^\^]+))(\^+|$)'] |
| added_regex_field | account |  | ['db-user=([^\\\^]+\\)?({account}({db_user}[^\^]+))(\^+|$)'] |
| removed_attribute | DupFields |  | N/A |
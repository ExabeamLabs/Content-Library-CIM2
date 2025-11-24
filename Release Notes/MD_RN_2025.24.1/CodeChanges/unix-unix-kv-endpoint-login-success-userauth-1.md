# Code Changes for unix-unix-kv-endpoint-login-success-userauth-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'account_name', 'additional_info', 'dest_host', 'event_name', 'host', 'host_ip', 'operation', 'operation_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'session_id', 'src_port', 'time', 'user_uid'] |
| edit_regex_field | host |  | ['({time}\d\d\d\d-\d+-\d+T\d\d:\d\d:\d\d\.\d+[-+]\d\d:\d\d)\s+({dest_host}({host}[\w.\-]+))', '\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d+-\d+T\d\d:\d\d:\d\d\.\d+[-+]\d\d:\d\d)\s+({dest_host}({host}[\w.\-]+))', 'msg=audit\(({time}\d{10})\.\d{3}'] |
| added_regex_field | dest_host |  | ['({time}\d\d\d\d-\d+-\d+T\d\d:\d\d:\d\d\.\d+[-+]\d\d:\d\d)\s+({dest_host}({host}[\w.\-]+))'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for microsoft-evsecurity-json-file-success-objectopen (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'auth_package', 'auth_process', 'dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'failure_reason', 'file_dir', 'host', 'login_id', 'login_type', 'object', 'object_class', 'operation_type', 'privileges', 'result', 'src_domain', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['ComputerName=({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['ComputerName=({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |
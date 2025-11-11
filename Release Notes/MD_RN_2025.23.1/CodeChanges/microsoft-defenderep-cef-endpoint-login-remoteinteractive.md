# Code Changes for microsoft-defenderep-cef-endpoint-login-remoteinteractive (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_host', 'dest_ip', 'dest_port', 'device_id', 'domain', 'event_name', 'hash_md5', 'host', 'login_id', 'login_type_text', 'process_command_line', 'process_id', 'process_name', 'process_path', 'protocol', 'result', 'time', 'user'] |
| edit_regex_field | host |  | ['"DeviceName":"({dest_host}({host}[\w\-.]+))"'] |
| added_regex_field | dest_host |  | ['"DeviceName":"({dest_host}({host}[\w\-.]+))"'] |
| removed_attribute | DupFields |  | N/A |
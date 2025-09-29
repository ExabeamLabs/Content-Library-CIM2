# Code Changes for microsoft-evsecurity-kv-endpoint-login-success-successfullyloggedon (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_host', 'dest_login_id', 'domain', 'event_code', 'event_name', 'host', 'key_length', 'login_id', 'login_type', 'process_dir', 'process_name', 'process_path', 'src_host_windows', 'src_ip', 'subject_sid', 'time', 'user', 'user_sid', 'user_upn'] |
| edit_regex_field | dest_host |  | ['Computer(\w+)?[\"\s]*(:|=)\s*\"?({dest_host}({host}[\w\-.]+?))(\"|\s|;)', 'ComputerName=({host}({dest_host}[\w\-\.]+))([^\s]*\s|;)'] |
| edit_regex_field | host |  | ['Computer(\w+)?[\"\s]*(:|=)\s*\"?({dest_host}({host}[\w\-.]+?))(\"|\s|;)', 'ComputerHOST644=({host}[\w\-.]+)\s\w+=', 'ComputerName=({host}({dest_host}[\w\-\.]+))([^\s]*\s|;)', 'Computer_name:({host}[^\s]+)'] |
| edit_regex_field | src_host_windows |  | ['Workstation Name(:|=)\s*(-|[A-Fa-f:\d.]+|(?:\\+)?({src_host_windows}[\w.\-]+\$?))[\s;]*Source Network Address(:|=)'] |
| added_regex_field | dest_login_id |  | ['Linked Logon ID:\s*({dest_login_id}[^\s]+)'] |
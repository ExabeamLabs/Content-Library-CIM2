# Code Changes for microsoft-evsecurity-kv-user-switch-success-4648-2 (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['dest_domain', 'dest_service_name', 'dest_user', 'domain', 'event_code', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'src_domain', 'src_user', 'time', 'user'] | ['dest_domain', 'dest_service_name', 'dest_user', 'domain', 'event_code', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user'] |
| added_regex_field | src_ip | [] | ['\sOriginatingComputer=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*'] |
| added_regex_field | src_port | [] | ['\sOriginatingComputer=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*'] |
| edit_attribute | activity_type | ['endpoint-login:success'] | ['endpoint-login:success', 'user-switch:success'] |
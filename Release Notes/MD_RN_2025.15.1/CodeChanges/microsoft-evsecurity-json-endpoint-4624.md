# Code Changes for microsoft-evsecurity-json-endpoint-4624 (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['auth_package', 'auth_process', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'login_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'src_domain', 'src_host_windows', 'src_ip', 'src_mac', 'src_port', 'src_user', 'time', 'user', 'user_sid'] | ['auth_package', 'auth_process', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'login_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'src_domain', 'src_host_windows', 'src_ip', 'src_mac', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | event_id | ['EventRecordID>({event_id}[^<]+)<'] | ['"record_id":"({event_id}\d+)"', 'EventRecordID>({event_id}[^<]+)<'] |
| added_regex_field | result | [] | ['keywords":\["({result}[^"]+)"'] |
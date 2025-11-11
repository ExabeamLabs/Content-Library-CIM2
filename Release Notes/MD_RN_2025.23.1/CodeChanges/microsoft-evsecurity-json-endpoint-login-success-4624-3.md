# Code Changes for microsoft-evsecurity-json-endpoint-login-success-4624-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'auth_package', 'auth_process', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'key_length', 'login_id', 'login_type', 'process_path', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'subject_sid', 'time', 'user', 'user_sid'] |
| edit_regex_field | src_host_windows |  | ['"network_information-WorkstationName":"\s*(-|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_host_windows}({src_host}[\w\-.]+)))\s*"'] |
| edit_regex_field | user |  | ['"new_logon-AccountName":"\s*({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"'] |
| added_regex_field | account |  | ['"new_logon-AccountName":"\s*({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"'] |
| added_regex_field | src_host |  | ['"network_information-WorkstationName":"\s*(-|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_host_windows}({src_host}[\w\-.]+)))\s*"'] |
| removed_attribute | DupFields |  | N/A |
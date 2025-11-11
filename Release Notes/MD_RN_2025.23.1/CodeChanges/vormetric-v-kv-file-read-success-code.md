# Code Changes for vormetric-v-kv-file-read-success-code (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'action', 'alert_name', 'dest_host', 'domain', 'file_dir', 'file_ext', 'file_name', 'group_id', 'group_name', 'key_name', 'policy_name', 'process_dir', 'process_name', 'process_path', 'time', 'user', 'user_id', 'user_info'] |
| edit_regex_field | domain |  | ['\suinfo=\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\+[^\"]*?({domain}[^,\"\\]+))?'] |
| edit_regex_field | user |  | ['\suinfo=\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\+[^\"]*?({domain}[^,\"\\]+))?'] |
| added_regex_field | group_id |  | ['\sgid=({group_id}\d+)\\\+({group_name}[^\\]+)'] |
| added_regex_field | group_name |  | ['\sgid=({group_id}\d+)\\\+({group_name}[^\\]+)'] |
| added_regex_field | key_name |  | ['\skey=\"({key_name}[^\"]+)\"'] |
| added_regex_field | policy_name |  | ['\spol=\"({policy_name}[^\"]+)\"'] |
| added_regex_field | user_id |  | ['\suid=({user_id}\d+)'] |
| added_regex_field | user_info |  | ['\suinfo=\"({user_info}[^"]+)'] |
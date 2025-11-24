# Code Changes for cyberark-pam-kv-app-activity-auditrecord (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'db_name', 'dest_host', 'dest_ip', 'dest_user', 'device_type', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'object', 'operation', 'record_type', 'result_reason', 'safe_name', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | file_dir |  | ['\sfname="(-|({object}({file_path}({file_dir}[^"=]*?[\\\/]+)?({file_name}[^"=\\\/]+?(\.({file_ext}\w+))?))))"'] |
| edit_regex_field | file_ext |  | ['\sfname="(-|({object}({file_path}({file_dir}[^"=]*?[\\\/]+)?({file_name}[^"=\\\/]+?(\.({file_ext}\w+))?))))"'] |
| edit_regex_field | file_name |  | ['\sfname="(-|({object}({file_path}({file_dir}[^"=]*?[\\\/]+)?({file_name}[^"=\\\/]+?(\.({file_ext}\w+))?))))"'] |
| edit_regex_field | file_path |  | ['\sfname="(-|({object}({file_path}({file_dir}[^"=]*?[\\\/]+)?({file_name}[^"=\\\/]+?(\.({file_ext}\w+))?))))"'] |
| edit_regex_field | operation |  | ['\sact="({event_name}({operation}[^"=]+))"'] |
| added_regex_field | event_name |  | ['\sact="({event_name}({operation}[^"=]+))"'] |
| added_regex_field | object |  | ['\sfname="(-|({object}({file_path}({file_dir}[^"=]*?[\\\/]+)?({file_name}[^"=\\\/]+?(\.({file_ext}\w+))?))))"'] |
| removed_attribute | DupFields |  | N/A |
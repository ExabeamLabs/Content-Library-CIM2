# Code Changes for cyberark-pam-cef-file-safe (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'action', 'additional_info', 'app', 'client_name', 'dest_domain', 'dest_host', 'dest_ip', 'dest_port', 'dest_user', 'device_type', 'domain', 'email_address', 'email_domain', 'error_info', 'event_code', 'event_name', 'failure_code', 'failure_reason', 'file_dir', 'file_ext', 'file_name', 'file_type', 'host', 'object', 'operation', 'protocol', 'result_reason', 'safe_name', 'severity', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | file_dir |  | ['\sfname="?(|({src_file_path}({file_dir}[^="]*?[\\\/]+)?({file_name}({object}({src_file_name}[^="\\\/]+?(\.({file_ext}({src_file_ext}\w+)))?)))))"?(\s+\w+=|\s*$)'] |
| edit_regex_field | operation |  | ['\Wact="?({access}({operation}[^"=\[\]]+?))"?(\[|\]|\s+\w+=|\s*$)'] |
| edit_regex_field | src_file_ext |  | ['\sfname="?(|({src_file_path}({file_dir}[^="]*?[\\\/]+)?({file_name}({object}({src_file_name}[^="\\\/]+?(\.({file_ext}({src_file_ext}\w+)))?)))))"?(\s+\w+=|\s*$)'] |
| edit_regex_field | src_file_name |  | ['\sfname="?(|({src_file_path}({file_dir}[^="]*?[\\\/]+)?({file_name}({object}({src_file_name}[^="\\\/]+?(\.({file_ext}({src_file_ext}\w+)))?)))))"?(\s+\w+=|\s*$)'] |
| edit_regex_field | src_file_path |  | ['\sfname="?(|({src_file_path}({file_dir}[^="]*?[\\\/]+)?({file_name}({object}({src_file_name}[^="\\\/]+?(\.({file_ext}({src_file_ext}\w+)))?)))))"?(\s+\w+=|\s*$)'] |
| added_regex_field | access |  | ['\Wact="?({access}({operation}[^"=\[\]]+?))"?(\[|\]|\s+\w+=|\s*$)'] |
| added_regex_field | file_ext |  | ['\sfname="?(|({src_file_path}({file_dir}[^="]*?[\\\/]+)?({file_name}({object}({src_file_name}[^="\\\/]+?(\.({file_ext}({src_file_ext}\w+)))?)))))"?(\s+\w+=|\s*$)'] |
| added_regex_field | file_name |  | ['\sfname="?(|({src_file_path}({file_dir}[^="]*?[\\\/]+)?({file_name}({object}({src_file_name}[^="\\\/]+?(\.({file_ext}({src_file_ext}\w+)))?)))))"?(\s+\w+=|\s*$)'] |
| added_regex_field | object |  | ['\sfname="?(|({src_file_path}({file_dir}[^="]*?[\\\/]+)?({file_name}({object}({src_file_name}[^="\\\/]+?(\.({file_ext}({src_file_ext}\w+)))?)))))"?(\s+\w+=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |
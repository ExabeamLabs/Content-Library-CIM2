# Code Changes for symantec-cloudsoc-cef-file-activity-symanteccloudsoc (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'additional_info', 'alert_severity', 'alert_type', 'app', 'browser', 'email_address', 'email_domain', 'file_dir', 'full_name', 'object', 'object_type', 'operation', 'resource', 'service_name', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_ip', 'src_port', 'target', 'time', 'user_agent'] |
| edit_regex_field | app |  | ['"service":"({service_name}({app}[^"]+))"'] |
| edit_regex_field | file_dir |  | ['"name":"(|\/|({object}({resource}({src_file_path}({file_dir}[^=]*?[\\\/]+\\\/)?(|({src_file_name}[^\\\/=]*?(\.({src_file_ext}[^"]+))?)?)))))"', '"object_name":"(|\/|({object}({resource}({src_file_path}({file_dir}[^=]*?[\\\/]+\\\/)?(|({src_file_name}[^\\\/=]*?(\.({src_file_ext}[^"]+))?)?)))))"'] |
| edit_regex_field | object |  | ['"name":"(|\/|({object}({resource}({src_file_path}({file_dir}[^=]*?[\\\/]+\\\/)?(|({src_file_name}[^\\\/=]*?(\.({src_file_ext}[^"]+))?)?)))))"', '"object_name":"(|\/|({object}({resource}({src_file_path}({file_dir}[^=]*?[\\\/]+\\\/)?(|({src_file_name}[^\\\/=]*?(\.({src_file_ext}[^"]+))?)?)))))"'] |
| edit_regex_field | operation |  | ['"activity_type":"({access}({operation}[^"]+))"'] |
| edit_regex_field | src_file_ext |  | ['"name":"(|\/|({object}({resource}({src_file_path}({file_dir}[^=]*?[\\\/]+\\\/)?(|({src_file_name}[^\\\/=]*?(\.({src_file_ext}[^"]+))?)?)))))"', '"object_name":"(|\/|({object}({resource}({src_file_path}({file_dir}[^=]*?[\\\/]+\\\/)?(|({src_file_name}[^\\\/=]*?(\.({src_file_ext}[^"]+))?)?)))))"'] |
| edit_regex_field | src_file_name |  | ['"name":"(|\/|({object}({resource}({src_file_path}({file_dir}[^=]*?[\\\/]+\\\/)?(|({src_file_name}[^\\\/=]*?(\.({src_file_ext}[^"]+))?)?)))))"', '"object_name":"(|\/|({object}({resource}({src_file_path}({file_dir}[^=]*?[\\\/]+\\\/)?(|({src_file_name}[^\\\/=]*?(\.({src_file_ext}[^"]+))?)?)))))"'] |
| edit_regex_field | src_file_path |  | ['"name":"(|\/|({object}({resource}({src_file_path}({file_dir}[^=]*?[\\\/]+\\\/)?(|({src_file_name}[^\\\/=]*?(\.({src_file_ext}[^"]+))?)?)))))"', '"object_name":"(|\/|({object}({resource}({src_file_path}({file_dir}[^=]*?[\\\/]+\\\/)?(|({src_file_name}[^\\\/=]*?(\.({src_file_ext}[^"]+))?)?)))))"'] |
| added_regex_field | access |  | ['"activity_type":"({access}({operation}[^"]+))"'] |
| added_regex_field | resource |  | ['"name":"(|\/|({object}({resource}({src_file_path}({file_dir}[^=]*?[\\\/]+\\\/)?(|({src_file_name}[^\\\/=]*?(\.({src_file_ext}[^"]+))?)?)))))"', '"object_name":"(|\/|({object}({resource}({src_file_path}({file_dir}[^=]*?[\\\/]+\\\/)?(|({src_file_name}[^\\\/=]*?(\.({src_file_ext}[^"]+))?)?)))))"'] |
| added_regex_field | service_name |  | ['"service":"({service_name}({app}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |
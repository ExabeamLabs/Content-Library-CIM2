# Code Changes for pan-cortex-kv-alert-trigger-success-true (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'domain', 'file_dir', 'file_ext', 'file_name', 'file_path', 'malware_file_name', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | file_dir |  | ['"+\[\"+(?:[A-Fa-f\d:.]+).+?\"+\]\"+,([^,]*,){17}({file_path}({file_dir}[^\"][^,]*?[\\\/]+)?({malware_file_name}({file_name}[^\\\/]*?(\.({file_ext}\w+))?))),'] |
| edit_regex_field | file_ext |  | ['"+\[\"+(?:[A-Fa-f\d:.]+).+?\"+\]\"+,([^,]*,){17}({file_path}({file_dir}[^\"][^,]*?[\\\/]+)?({malware_file_name}({file_name}[^\\\/]*?(\.({file_ext}\w+))?))),'] |
| edit_regex_field | file_name |  | ['"+\[\"+(?:[A-Fa-f\d:.]+).+?\"+\]\"+,([^,]*,){17}({file_path}({file_dir}[^\"][^,]*?[\\\/]+)?({malware_file_name}({file_name}[^\\\/]*?(\.({file_ext}\w+))?))),'] |
| edit_regex_field | file_path |  | ['"+\[\"+(?:[A-Fa-f\d:.]+).+?\"+\]\"+,([^,]*,){17}({file_path}({file_dir}[^\"][^,]*?[\\\/]+)?({malware_file_name}({file_name}[^\\\/]*?(\.({file_ext}\w+))?))),'] |
| added_regex_field | malware_file_name |  | ['"+\[\"+(?:[A-Fa-f\d:.]+).+?\"+\]\"+,([^,]*,){17}({file_path}({file_dir}[^\"][^,]*?[\\\/]+)?({malware_file_name}({file_name}[^\\\/]*?(\.({file_ext}\w+))?))),'] |
| removed_attribute | DupFields |  | N/A |
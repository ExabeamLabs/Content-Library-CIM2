# Code Changes for microsoft-sysmon-json-registry-success-12 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'process_dir', 'process_name', 'process_path', 'registry_path', 'target', 'user'] |
| edit_regex_field | file_dir |  | ['exa_json_path=$.winlog.event_data.TargetObject,exa_regex=^({registry_path}({target}({file_path}({file_dir}[^",]*?)\s*({file_name}[^\\",]+?(\.({file_ext}\w+))?))))$'] |
| edit_regex_field | file_ext |  | ['exa_json_path=$.winlog.event_data.TargetObject,exa_regex=^({registry_path}({target}({file_path}({file_dir}[^",]*?)\s*({file_name}[^\\",]+?(\.({file_ext}\w+))?))))$'] |
| edit_regex_field | file_name |  | ['exa_json_path=$.winlog.event_data.TargetObject,exa_regex=^({registry_path}({target}({file_path}({file_dir}[^",]*?)\s*({file_name}[^\\",]+?(\.({file_ext}\w+))?))))$'] |
| edit_regex_field | file_path |  | ['exa_json_path=$.winlog.event_data.TargetObject,exa_regex=^({registry_path}({target}({file_path}({file_dir}[^",]*?)\s*({file_name}[^\\",]+?(\.({file_ext}\w+))?))))$'] |
| added_regex_field | registry_path |  | ['exa_json_path=$.winlog.event_data.TargetObject,exa_regex=^({registry_path}({target}({file_path}({file_dir}[^",]*?)\s*({file_name}[^\\",]+?(\.({file_ext}\w+))?))))$'] |
| added_regex_field | target |  | ['exa_json_path=$.winlog.event_data.TargetObject,exa_regex=^({registry_path}({target}({file_path}({file_dir}[^",]*?)\s*({file_name}[^\\",]+?(\.({file_ext}\w+))?))))$'] |
| removed_attribute | DupFields |  | N/A |
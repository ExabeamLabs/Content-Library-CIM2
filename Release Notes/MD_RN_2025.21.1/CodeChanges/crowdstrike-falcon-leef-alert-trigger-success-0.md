# Code Changes for crowdstrike-falcon-leef-alert-trigger-success-0 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'app', 'category', 'dest_ip', 'dest_port', 'domain', 'file_dir', 'file_name', 'hash_md5', 'hash_sha256', 'malware_url', 'process_command_line', 'process_name', 'process_path', 'protocol', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | category |  | ['\Wcat=({alert_type}({category}[^\|]+?))\s*(\||\w+=|$|"+\s*$)'] |
| edit_regex_field | file_dir |  | ['\WfilePath=({malware_url}({file_dir}.+?))(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)'] |
| added_regex_field | alert_type |  | ['\Wcat=({alert_type}({category}[^\|]+?))\s*(\||\w+=|$|"+\s*$)'] |
| added_regex_field | malware_url |  | ['\WfilePath=({malware_url}({file_dir}.+?))(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)'] |
| removed_attribute | DupFields |  | N/A |
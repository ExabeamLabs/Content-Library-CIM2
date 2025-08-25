# Code Changes for crowdstrike-falcon-leef-file-write-success-executableswritten (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'app', 'category', 'dest_ip', 'dest_port', 'domain', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'protocol', 'src_file_name', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | file_name |  | ['\WexeWrittenFileName=({file_name}[^|"]+?)(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)', '\WexeWrittenFilePath=({file_path}({file_dir}[^=]+?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)'] |
| edit_regex_field | file_path |  | ['\WexeWrittenFilePath=({file_path}({file_dir}[^=]+?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)'] |
| added_regex_field | file_dir |  | ['\WexeWrittenFilePath=({file_path}({file_dir}[^=]+?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)'] |
| added_regex_field | file_ext |  | ['\WexeWrittenFilePath=({file_path}({file_dir}[^=]+?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))(\t|\s+\w+=|\s*\||\s*$|\s*"+\s*$)'] |
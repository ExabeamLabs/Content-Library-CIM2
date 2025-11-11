# Code Changes for microsoft-mcas-cef-file-download-success-downloadfile (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'additional_info', 'app', 'email_address', 'file_dir', 'file_ext', 'file_name', 'file_path', 'file_type', 'host', 'operation', 'src_file_name', 'src_ip', 'time', 'user'] |
| edit_regex_field | file_dir |  | ['\Wmsg=(.+?):\s*({file_type}[^\s]+)\s+({file_path}({file_dir}[^=]+?)[\\\/]+(|({file_name}({src_file_name}[^\\\/]*?(\.({file_ext}[^\\\/:\s\.]+))?))))(\s*(with|folder|to file|;)\s+.*?)?\s+(?:$|\w+=)'] |
| edit_regex_field | file_ext |  | ['\Wmsg=(.+?):\s*({file_type}[^\s]+)\s+({file_path}({file_dir}[^=]+?)[\\\/]+(|({file_name}({src_file_name}[^\\\/]*?(\.({file_ext}[^\\\/:\s\.]+))?))))(\s*(with|folder|to file|;)\s+.*?)?\s+(?:$|\w+=)'] |
| edit_regex_field | file_path |  | ['\Wmsg=(.+?):\s*({file_type}[^\s]+)\s+({file_path}({file_dir}[^=]+?)[\\\/]+(|({file_name}({src_file_name}[^\\\/]*?(\.({file_ext}[^\\\/:\s\.]+))?))))(\s*(with|folder|to file|;)\s+.*?)?\s+(?:$|\w+=)'] |
| edit_regex_field | file_type |  | ['\Wmsg=(.+?):\s*({file_type}[^\s]+)\s+({file_path}({file_dir}[^=]+?)[\\\/]+(|({file_name}({src_file_name}[^\\\/]*?(\.({file_ext}[^\\\/:\s\.]+))?))))(\s*(with|folder|to file|;)\s+.*?)?\s+(?:$|\w+=)'] |
| edit_regex_field | src_file_name |  | ['\Wmsg=(.+?):\s*({file_type}[^\s]+)\s+({file_path}({file_dir}[^=]+?)[\\\/]+(|({file_name}({src_file_name}[^\\\/]*?(\.({file_ext}[^\\\/:\s\.]+))?))))(\s*(with|folder|to file|;)\s+.*?)?\s+(?:$|\w+=)'] |
| added_regex_field | file_name |  | ['\Wmsg=(.+?):\s*({file_type}[^\s]+)\s+({file_path}({file_dir}[^=]+?)[\\\/]+(|({file_name}({src_file_name}[^\\\/]*?(\.({file_ext}[^\\\/:\s\.]+))?))))(\s*(with|folder|to file|;)\s+.*?)?\s+(?:$|\w+=)'] |
| removed_attribute | DupFields |  | N/A |
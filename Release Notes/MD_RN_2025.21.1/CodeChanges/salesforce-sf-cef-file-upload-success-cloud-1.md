# Code Changes for salesforce-sf-cef-file-upload-success-cloud-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'email_address', 'file_ext', 'file_name', 'file_path', 'file_type', 'full_name', 'operation', 'src_file_ext', 'src_file_name', 'time', 'user'] |
| edit_regex_field | file_ext |  | ['\Wfname=({file_name}({src_file_name}.+?(?:\.({src_file_ext}({file_ext}[^".]+?)))?))\s+(\w+=|$)'] |
| edit_regex_field | src_file_name |  | ['\Wfname=({file_name}({src_file_name}.+?(?:\.({src_file_ext}({file_ext}[^".]+?)))?))\s+(\w+=|$)'] |
| added_regex_field | file_name |  | ['\Wfname=({file_name}({src_file_name}.+?(?:\.({src_file_ext}({file_ext}[^".]+?)))?))\s+(\w+=|$)'] |
| added_regex_field | src_file_ext |  | ['\Wfname=({file_name}({src_file_name}.+?(?:\.({src_file_ext}({file_ext}[^".]+?)))?))\s+(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |
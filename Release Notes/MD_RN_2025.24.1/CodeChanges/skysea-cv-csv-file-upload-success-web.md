# Code Changes for skysea-cv-csv-file-upload-success-web (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'app', 'domain', 'file_ext', 'file_name', 'host', 'src_file_dir', 'src_file_ext', 'src_file_name', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | src_file_dir |  | ['Webアップロード,([^,]*,){23}(({src_file_dir}[^=]+?)\\+)?({file_name}({src_file_name}[^\\]+?(\.({file_ext}({src_file_ext}[^\\,\.]+)))?)),'] |
| edit_regex_field | src_file_ext |  | ['Webアップロード,([^,]*,){23}(({src_file_dir}[^=]+?)\\+)?({file_name}({src_file_name}[^\\]+?(\.({file_ext}({src_file_ext}[^\\,\.]+)))?)),'] |
| edit_regex_field | src_file_name |  | ['Webアップロード,([^,]*,){23}(({src_file_dir}[^=]+?)\\+)?({file_name}({src_file_name}[^\\]+?(\.({file_ext}({src_file_ext}[^\\,\.]+)))?)),'] |
| added_regex_field | file_ext |  | ['Webアップロード,([^,]*,){23}(({src_file_dir}[^=]+?)\\+)?({file_name}({src_file_name}[^\\]+?(\.({file_ext}({src_file_ext}[^\\,\.]+)))?)),'] |
| added_regex_field | file_name |  | ['Webアップロード,([^,]*,){23}(({src_file_dir}[^=]+?)\\+)?({file_name}({src_file_name}[^\\]+?(\.({file_ext}({src_file_ext}[^\\,\.]+)))?)),'] |
| removed_attribute | DupFields |  | N/A |
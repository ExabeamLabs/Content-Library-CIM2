# Code Changes for skysea-cv-csv-file-download-success-web (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'download_source', 'file_dir', 'file_ext', 'file_name', 'host', 'src_file_ext', 'src_file_name', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | file_dir |  | ['Webアクセス,([^,]*,){32}(({file_dir}[^=]+?)\\+)?({file_name}({src_file_name}[^\\]+?(\.({file_ext}({src_file_ext}[^\\,\.]+)))?)),'] |
| edit_regex_field | src_file_ext |  | ['Webアクセス,([^,]*,){32}(({file_dir}[^=]+?)\\+)?({file_name}({src_file_name}[^\\]+?(\.({file_ext}({src_file_ext}[^\\,\.]+)))?)),'] |
| edit_regex_field | src_file_name |  | ['Webアクセス,([^,]*,){32}(({file_dir}[^=]+?)\\+)?({file_name}({src_file_name}[^\\]+?(\.({file_ext}({src_file_ext}[^\\,\.]+)))?)),'] |
| added_regex_field | file_ext |  | ['Webアクセス,([^,]*,){32}(({file_dir}[^=]+?)\\+)?({file_name}({src_file_name}[^\\]+?(\.({file_ext}({src_file_ext}[^\\,\.]+)))?)),'] |
| added_regex_field | file_name |  | ['Webアクセス,([^,]*,){32}(({file_dir}[^=]+?)\\+)?({file_name}({src_file_name}[^\\]+?(\.({file_ext}({src_file_ext}[^\\,\.]+)))?)),'] |
| removed_attribute | DupFields |  | N/A |
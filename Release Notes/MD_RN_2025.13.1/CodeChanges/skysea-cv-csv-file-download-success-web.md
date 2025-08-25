# Code Changes for skysea-cv-csv-file-download-success-web (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'download_source', 'file_dir', 'host', 'src_file_ext', 'src_file_name', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| removed_regex_field | file_path |  | [] |
| edit_regex_field | src_file_ext |  | ['Webアクセス,([^,]*,){32}(({file_dir}[^=]+?)\\+)?({src_file_name}[^\\]+?(\.({src_file_ext}[^\\,\.]+))?),'] |
| edit_regex_field | src_file_name |  | ['Webアクセス,([^,]*,){32}(({file_dir}[^=]+?)\\+)?({src_file_name}[^\\]+?(\.({src_file_ext}[^\\,\.]+))?),'] |
| added_regex_field | file_dir |  | ['Webアクセス,([^,]*,){32}(({file_dir}[^=]+?)\\+)?({src_file_name}[^\\]+?(\.({src_file_ext}[^\\,\.]+))?),'] |
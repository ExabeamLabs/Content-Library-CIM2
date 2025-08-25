# Code Changes for skyhighsecurity-swg-cef-file-download-success-filedownload (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | file_dir |  | ['\sSource_ID=({file_path}({file_dir}[^"]*?[\\\/]+)({file_name}[^\\\/"]+?(\.({file_ext}[^\\\/\.\s"]+))?))\s'] |
| edit_regex_field | file_ext |  | ['\sSource_ID=({file_path}({file_dir}[^"]*?[\\\/]+)({file_name}[^\\\/"]+?(\.({file_ext}[^\\\/\.\s"]+))?))\s'] |
| edit_regex_field | file_name |  | ['\sSource_ID=({file_path}({file_dir}[^"]*?[\\\/]+)({file_name}[^\\\/"]+?(\.({file_ext}[^\\\/\.\s"]+))?))\s'] |
| edit_regex_field | file_path |  | ['\sSource_ID=({file_path}({file_dir}[^"]*?[\\\/]+)({file_name}[^\\\/"]+?(\.({file_ext}[^\\\/\.\s"]+))?))\s'] |
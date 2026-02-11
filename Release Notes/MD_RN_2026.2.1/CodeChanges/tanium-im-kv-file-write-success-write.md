# Code Changes for tanium-im-kv-file-write-success-write (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | [' Computer-Name="', ' File-Path="', ' Process-Path="', ' Tanium ', 'Change-Type='] |
| changed_parsed_fields | N/A |  | ['dest_host', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'host', 'process_name', 'process_path', 'src_file_path', 'time', 'user'] |
| edit_regex_field | event_name |  | ['Change-Type="({event_name}[^"]+)"'] |
| edit_regex_field | file_dir |  | ['File-Path="({file_path}({file_dir}.*?)({file_name}[^\\\/;"]+?(\.({file_ext}[^\.;\\"]+?))?))"'] |
| edit_regex_field | file_ext |  | ['File-Path="({file_path}({file_dir}.*?)({file_name}[^\\\/;"]+?(\.({file_ext}[^\.;\\"]+?))?))"'] |
| edit_regex_field | file_name |  | ['File-Path="({file_path}({file_dir}.*?)({file_name}[^\\\/;"]+?(\.({file_ext}[^\.;\\"]+?))?))"'] |
| edit_regex_field | file_path |  | ['File-Path="({file_path}({file_dir}.*?)({file_name}[^\\\/;"]+?(\.({file_ext}[^\.;\\"]+?))?))"'] |
| added_regex_field | hash_md5 |  | ['Hash=({hash_md5}[^"]+?)'] |
| edit_attribute | activity_type |  | ['file-create:success', 'file-write:success'] |
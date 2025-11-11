# Code Changes for microsoft-o365-sk4-file-write-success-filecreatedonremovablemedia (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes', 'dest_host', 'device_id', 'device_type', 'domain', 'email_address', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'first_name', 'full_name', 'hash_sha1', 'hash_sha256', 'host', 'last_name', 'operation', 'process_name', 'src_file_ext', 'src_file_name', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | file_dir |  | ['"ObjectId":"({file_path}({file_dir}[^"]+?)\\+({src_file_name}({file_name}[^\\"]+)))"'] |
| edit_regex_field | file_ext |  | ['"FileExtension":"({src_file_ext}({file_ext}[^"]+))"'] |
| edit_regex_field | file_name |  | ['"ObjectId":"({file_path}({file_dir}[^"]+?)\\+({src_file_name}({file_name}[^\\"]+)))"'] |
| edit_regex_field | file_path |  | ['"ObjectId":"({file_path}({file_dir}[^"]+?)\\+({src_file_name}({file_name}[^\\"]+)))"'] |
| edit_regex_field | host |  | ['"DeviceName":"(::ffff:)?({dest_host}({host}[\w\-.]+))"'] |
| edit_regex_field | operation |  | ['"Operation":"({event_name}({operation}[^"]*))"'] |
| added_regex_field | dest_host |  | ['"DeviceName":"(::ffff:)?({dest_host}({host}[\w\-.]+))"'] |
| added_regex_field | event_name |  | ['"Operation":"({event_name}({operation}[^"]*))"'] |
| added_regex_field | src_file_ext |  | ['"FileExtension":"({src_file_ext}({file_ext}[^"]+))"'] |
| added_regex_field | src_file_name |  | ['"ObjectId":"({file_path}({file_dir}[^"]+?)\\+({src_file_name}({file_name}[^\\"]+)))"'] |
| removed_attribute | DupFields |  | N/A |
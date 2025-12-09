# Code Changes for box-ccm-cef-file-success-move (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'app', 'bytes', 'dest_email_address', 'dest_email_domain', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'file_type', 'full_name', 'process_name', 'src_file_ext', 'src_file_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | file_ext |  | ['"source":.*?"item_name":"({src_file_name}({file_name}[^"]+?(\.({src_file_ext}({file_ext}[^"\s]+)))?))"'] |
| edit_regex_field | file_name |  | ['"source":.*?"item_name":"({src_file_name}({file_name}[^"]+?(\.({src_file_ext}({file_ext}[^"\s]+)))?))"'] |
| added_regex_field | src_file_ext |  | ['"source":.*?"item_name":"({src_file_name}({file_name}[^"]+?(\.({src_file_ext}({file_ext}[^"\s]+)))?))"'] |
| added_regex_field | src_file_name |  | ['"source":.*?"item_name":"({src_file_name}({file_name}[^"]+?(\.({src_file_ext}({file_ext}[^"\s]+)))?))"'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for ipswitch-mdmz-kv-file-download-success-moveitdownload (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_id', 'file_name', 'full_name', 'host', 'operation', 'src_ip', 'src_port', 'time', 'user'] |
| removed_regex_field | file_path |  | [] |
| added_regex_field | file_dir |  | ['\sFolderPath:\s*({file_dir}[^,]+)'] |
# Code Changes for crowdstrike-falcon-mix-alert-trigger-success-suspiciousactivity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'additional_info_1', 'additional_info_2', 'alert_id', 'alert_name', 'alert_severity', 'alert_source', 'alert_type', 'category', 'cid', 'dest_host', 'dest_ip', 'dest_port', 'disposition', 'email_address', 'falcon_host_link', 'file_path', 'grandparent_command_line', 'grandparent_image_filename', 'hash_md5', 'hash_sha256', 'parent_image_filename', 'parent_process_command_line', 'parent_process_guid', 'process_command_line', 'process_guid', 'process_name', 'protocol', 'sensor_id', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| removed_regex_field | process_dir |  | [] |
| edit_regex_field | process_name |  | ['"FileName":\s*"({process_name}[^"]+)"'] |
| removed_regex_field | process_path |  | [] |
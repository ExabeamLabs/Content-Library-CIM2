# Code Changes for microsoft-o365-sk4-file-delete-success-filedeleted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'correlation_id', 'dest_ip', 'dest_port', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'host', 'object', 'operation', 'result', 'src_file_name', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| removed_regex_field | file_path |  | [] |
| added_regex_field | file_dir |  | ['"SourceRelativeUrl":"({file_dir}[^"]+)"'] |
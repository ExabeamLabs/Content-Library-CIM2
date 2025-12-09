# Code Changes for microsoft-o365-sk4-file-delete-success-filedeleted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'correlation_id', 'dest_ip', 'dest_port', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'host', 'object', 'operation', 'resource', 'result', 'src_file_name', 'src_ip', 'src_port', 'time', 'url', 'user', 'user_agent'] |
| added_regex_field | url |  | ['"SiteUrl":"({url}[^"]+)"'] |
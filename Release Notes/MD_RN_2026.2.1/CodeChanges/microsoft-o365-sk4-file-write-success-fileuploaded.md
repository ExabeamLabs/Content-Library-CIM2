# Code Changes for microsoft-o365-sk4-file-write-success-fileuploaded (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'auth_type', 'browser', 'category', 'connection_id', 'email_address', 'email_domain', 'file_name', 'log_source', 'object', 'object_id', 'object_type', 'operation', 'resource', 'result', 'src_file_dir', 'src_ip', 'src_port', 'time', 'url', 'user_type', 'web_domain'] |
| added_regex_field | url |  | ['"SiteUrl":\s*"({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*)'] |
| added_regex_field | web_domain |  | ['"SiteUrl":\s*"({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*)'] |
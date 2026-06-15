# Code Changes for microsoft-o365-sk4-file-write-success-filemodified (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'auth_type', 'browser', 'bytes', 'category', 'connection_id', 'email_address', 'log_source', 'object', 'object_id', 'object_type', 'operation', 'os', 'resource', 'result', 'site_name', 'src_file_dir', 'src_file_ext', 'src_file_name', 'src_ip', 'src_port', 'time', 'url', 'web_domain'] |
| edit_regex_field | email_address |  | ['"(UserId|userPrincipalName)":"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"', 'exa_json_path=$.UserId,exa_regex=^({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)$'] |
| edit_regex_field | url |  | ['"SiteUrl":\s*"({site_name}({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*))', 'exa_json_path=$.SiteUrl,exa_regex=({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*)'] |
| edit_regex_field | web_domain |  | ['"SiteUrl":\s*"({site_name}({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*))', 'exa_json_path=$.SiteUrl,exa_regex=({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*)'] |
| added_regex_field | site_name |  | ['"SiteUrl":\s*"({site_name}({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*))'] |
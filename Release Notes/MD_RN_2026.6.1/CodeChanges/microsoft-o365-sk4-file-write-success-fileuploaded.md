# Code Changes for microsoft-o365-sk4-file-write-success-fileuploaded (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'app_id', 'auth_type', 'browser', 'category', 'connection_id', 'email_address', 'file_name', 'log_source', 'object', 'object_id', 'object_type', 'operation', 'resource', 'result', 'site_name', 'src_file_dir', 'src_ip', 'src_port', 'time', 'url', 'user_type', 'web_domain'] |
| edit_regex_field | email_address |  | ['"(UserId|userPrincipalName)":"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"'] |
| edit_regex_field | url |  | ['"SiteUrl":\s*"({site_name}({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*))'] |
| edit_regex_field | web_domain |  | ['"SiteUrl":\s*"({site_name}({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*))'] |
| added_regex_field | app_id |  | ['"ApplicationId":\s*"({app_id}[^"]+)"'] |
| added_regex_field | site_name |  | ['"SiteUrl":\s*"({site_name}({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*))'] |
# Code Changes for microsoft-o365-sk4-file-app-userkey (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'app_id', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'file_path', 'object', 'object_id', 'object_type', 'operation', 'policy_name', 'removable_media_serial_number', 'removable_media_vendor', 'site_name', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_host', 'src_ip', 'src_port', 'tenant_id', 'time', 'url', 'user_agent', 'user_type', 'web_domain'] |
| edit_regex_field | email_address |  | ['"UserId":\s*"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)",', 'exa_json_path=$.UserId,exa_regex=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.UserId,exa_regex=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | url |  | ['"SiteUrl":"({site_name}({url}[^"]+))"', '"SiteUrl":\s*"({site_name}({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*))', 'exa_json_path=$.SiteUrl,exa_regex=({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*)'] |
| edit_regex_field | web_domain |  | ['"SiteUrl":\s*"({site_name}({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*))', 'exa_json_path=$.SiteUrl,exa_regex=({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*)'] |
| added_regex_field | app_id |  | ['"ApplicationId":"({app_id}[^"]+)"', '"ApplicationId":\s*"({app_id}[^"]+)"'] |
| added_regex_field | site_name |  | ['"SiteUrl":"({site_name}({url}[^"]+))"', '"SiteUrl":\s*"({site_name}({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*))'] |
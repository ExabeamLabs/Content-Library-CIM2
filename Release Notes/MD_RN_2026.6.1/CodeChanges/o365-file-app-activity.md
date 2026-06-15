# Code Changes for o365-file-app-activity (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'app_id', 'email_address', 'email_domain', 'object', 'object_id', 'object_type', 'operation', 'site_name', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_ip', 'src_port', 'tenant_id', 'time', 'url', 'user_agent', 'user_type'] |
| edit_regex_field | email_address |  | ['"UserId":\s*"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)",', 'exa_json_path=$.UserId,exa_regex=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.UserId,exa_regex=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| added_regex_field | app_id |  | ['"ApplicationId":"({app_id}[^"]+)"'] |
| added_regex_field | site_name |  | ['"SiteUrl":"({site_name}({url}[^"]+))"'] |
| added_regex_field | url |  | ['"SiteUrl":"({site_name}({url}[^"]+))"'] |
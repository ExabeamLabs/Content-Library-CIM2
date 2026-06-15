# Code Changes for microsoft-o365-sk4-file-delete-success-filedeleted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'correlation_id', 'dest_ip', 'dest_port', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'host', 'object', 'operation', 'resource', 'result', 'site_name', 'src_file_name', 'src_ip', 'src_port', 'time', 'url', 'user', 'user_agent'] |
| edit_regex_field | email_address |  | ['"(UserId|userPrincipalName)":"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | email_domain |  | ['"(UserId|userPrincipalName)":"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | url |  | ['"SiteUrl":"({site_name}({url}[^"]+))"'] |
| edit_regex_field | user |  | ['"(UserId|userPrincipalName)":"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | site_name |  | ['"SiteUrl":"({site_name}({url}[^"]+))"'] |
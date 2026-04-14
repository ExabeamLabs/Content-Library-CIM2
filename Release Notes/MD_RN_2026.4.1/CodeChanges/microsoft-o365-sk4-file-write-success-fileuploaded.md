# Code Changes for microsoft-o365-sk4-file-write-success-fileuploaded (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'auth_type', 'browser', 'category', 'connection_id', 'email_address', 'file_name', 'log_source', 'object', 'object_id', 'object_type', 'operation', 'resource', 'result', 'src_file_dir', 'src_ip', 'src_port', 'time', 'url', 'user_type', 'web_domain'] |
| edit_regex_field | email_address |  | ['"(UserId|userPrincipalName)":"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"'] |
| removed_regex_field | email_domain |  | [] |
# Code Changes for netskope-sc-sk4-file-delete-success-folderdeleted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'action', 'app', 'auth_method', 'browser', 'bytes', 'dest_port', 'domain', 'email_address', 'file_name', 'file_type', 'full_name', 'location', 'object', 'operation', 'os', 'src_host', 'src_ip', 'src_port', 'time', 'url', 'user', 'web_domain'] |
| added_regex_field | access |  | ['"activity":\s*"({access}[^"]+)"'] |
| added_regex_field | file_name |  | ['"object":\s*"(\s+"|(\s*(Unknown Unknown|unknown|Unknown|null|({file_name}[^"]+?))\s*"))'] |
| removed_attribute | DupFields |  | N/A |
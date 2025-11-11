# Code Changes for netskope-sc-cef-app-login-fail-loginfailed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'app', 'auth_method', 'browser', 'bytes', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'file_type', 'full_name', 'location', 'mime', 'operation', 'os', 'referrer', 'src_host', 'src_ip', 'src_port', 'time', 'url', 'user', 'user_agent', 'web_domain'] |
| edit_regex_field | file_type |  | ['"file_type":\s*"({mime}({file_type}[^"]+))"'] |
| added_regex_field | mime |  | ['"file_type":\s*"({mime}({file_type}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |
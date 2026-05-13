# Code Changes for cisco-duo-cef-app-login-destservicenameduo (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'additional_info', 'alert_type', 'app', 'browser', 'dest_email_user', 'dest_user', 'device_name', 'email_address', 'email_domain', 'factor', 'failure_reason', 'full_name', 'object', 'operation', 'os', 'src_ip', 'src_port', 'status_msg', 'time', 'user'] |
| edit_regex_field | dest_email_user |  | ['"description":"\{\\"uname\\":\s\\"(({dest_email_user}[^"\s@]+@[^"\s@]+)|({dest_user}({account_name}[^"]+?)))\\?"'] |
| edit_regex_field | dest_user |  | ['"description":"\{\\"uname\\":\s\\"(({dest_email_user}[^"\s@]+@[^"\s@]+)|({dest_user}({account_name}[^"]+?)))\\?"'] |
| added_regex_field | account_name |  | ['"description":"\{\\"uname\\":\s\\"(({dest_email_user}[^"\s@]+@[^"\s@]+)|({dest_user}({account_name}[^"]+?)))\\?"'] |
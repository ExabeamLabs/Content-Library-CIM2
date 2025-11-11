# Code Changes for microsoft-evsecurity-cef-handle-request-success-4656 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'handle_id', 'host', 'login_id', 'object', 'object_id', 'object_server', 'object_type', 'operation_type', 'privileges', 'process_id', 'process_path', 'src_domain', 'src_user', 'thread_id', 'time', 'transaction_id', 'user', 'user_sid'] |
| edit_regex_field | access |  | ['"AccessList":"({privileges}({access}[^"]+))"'] |
| edit_regex_field | domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))"'] |
| edit_regex_field | host |  | ['"Computer":"({dest_host}({host}[^"]+))"'] |
| edit_regex_field | user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | dest_host |  | ['"Computer":"({dest_host}({host}[^"]+))"'] |
| added_regex_field | privileges |  | ['"AccessList":"({privileges}({access}[^"]+))"'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))"'] |
| added_regex_field | src_user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| removed_attribute | DupFields |  | N/A |
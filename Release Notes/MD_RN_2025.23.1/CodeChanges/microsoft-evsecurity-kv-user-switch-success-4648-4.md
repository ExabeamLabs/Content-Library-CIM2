# Code Changes for microsoft-evsecurity-kv-user-switch-success-4648-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'account_login_guid', 'dest_domain', 'dest_host', 'dest_service_name', 'dest_user', 'domain', 'event_code', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_login_guid', 'user_sid'] |
| edit_regex_field | dest_user |  | ['TargetUserName:({account}({dest_user}[^,]+)),'] |
| edit_regex_field | domain |  | ['SubjectDomainName:(-|({src_domain}({domain}[^,]+))),'] |
| edit_regex_field | user |  | ['SubjectUserName:(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))),'] |
| added_regex_field | account |  | ['TargetUserName:({account}({dest_user}[^,]+)),'] |
| added_regex_field | src_domain |  | ['SubjectDomainName:(-|({src_domain}({domain}[^,]+))),'] |
| added_regex_field | src_user |  | ['SubjectUserName:(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))),'] |
| removed_attribute | DupFields |  | N/A |
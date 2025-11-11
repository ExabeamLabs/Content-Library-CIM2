# Code Changes for microsoft-evsecurity-sk4-share-access-success-5140-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'd_name', 'd_parent', 'dest_host', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_type', 'host', 'log_source', 'login_id', 'share_name', 'share_path', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"SubjectDomainName":"(-|({src_domain}({domain}[^"]+)))'] |
| edit_regex_field | host |  | ['"Computer":"({dest_host}({host}[^"]+))"'] |
| edit_regex_field | user |  | ['"SubjectUserName":"(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| added_regex_field | dest_host |  | ['"Computer":"({dest_host}({host}[^"]+))"'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName":"(-|({src_domain}({domain}[^"]+)))'] |
| added_regex_field | src_user |  | ['"SubjectUserName":"(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| removed_attribute | DupFields |  | N/A |
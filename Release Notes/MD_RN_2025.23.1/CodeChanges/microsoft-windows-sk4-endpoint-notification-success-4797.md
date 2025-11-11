# Code Changes for microsoft-windows-sk4-endpoint-notification-success-4797 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'log_source', 'login_id', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"SubjectDomainName":"(-|({src_domain}({domain}[^"]+)))'] |
| edit_regex_field | src_host_windows |  | ['"Workstation":"({src_host_windows}({src_host}[^"]+))"'] |
| edit_regex_field | user |  | ['"SubjectUserName":"(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName":"(-|({src_domain}({domain}[^"]+)))'] |
| added_regex_field | src_host |  | ['"Workstation":"({src_host_windows}({src_host}[^"]+))"'] |
| added_regex_field | src_user |  | ['"SubjectUserName":"(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| removed_attribute | DupFields |  | N/A |
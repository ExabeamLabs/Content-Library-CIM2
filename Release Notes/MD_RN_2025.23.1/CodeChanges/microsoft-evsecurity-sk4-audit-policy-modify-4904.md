# Code Changes for microsoft-evsecurity-sk4-audit-policy-modify-4904 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'severity', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))"', 'Security ID:\s*(|({user_sid}[^\s:]+))\s+Account Name:\s*(|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+Account Domain:\s*(|({src_domain}({domain}[^\s]+)))\s+'] |
| edit_regex_field | user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'Security ID:\s*(|({user_sid}[^\s:]+))\s+Account Name:\s*(|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+Account Domain:\s*(|({src_domain}({domain}[^\s]+)))\s+'] |
| edit_regex_field | user_sid |  | ['"SubjectUserSid":"({user_sid}[^"]+)"', 'Security ID:\s*(|({user_sid}[^\s:]+))\s+Account Name:\s*(|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+Account Domain:\s*(|({src_domain}({domain}[^\s]+)))\s+'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))"', 'Security ID:\s*(|({user_sid}[^\s:]+))\s+Account Name:\s*(|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+Account Domain:\s*(|({src_domain}({domain}[^\s]+)))\s+'] |
| added_regex_field | src_user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'Security ID:\s*(|({user_sid}[^\s:]+))\s+Account Name:\s*(|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+Account Domain:\s*(|({src_domain}({domain}[^\s]+)))\s+'] |
| removed_attribute | DupFields |  | N/A |
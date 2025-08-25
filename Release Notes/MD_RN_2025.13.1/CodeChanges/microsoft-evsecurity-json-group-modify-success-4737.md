# Code Changes for microsoft-evsecurity-json-group-modify-success-4737 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ['epoch_sec', 'yyyy-MM-dd HH:mm:ss Z'] |
| edit_regex_field | domain |  | ['"SubjectDomainName":"({domain}[^"]+)"', 'exa_regex=Subject:.+?Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:\s+({domain}.+?)\s+Logon ID:\s+({login_id}[^\s]+)'] |
| edit_regex_field | event_name |  | ['({event_name}A security-enabled global group was changed)', 'exa_regex=({event_name}A security-enabled global group was changed)'] |
| edit_regex_field | group_id |  | ['"TargetSid":"({group_id}[^"]+)', 'exa_regex=Group: Security ID:\s*({group_id}[^\s]+)'] |
| edit_regex_field | group_name |  | ['"TargetUserName":"({group_name}[^"]+)', 'exa_regex=Group:.+?Group Name:\s*({group_name}[^\s]+)'] |
| edit_regex_field | login_id |  | ['"SubjectLogonId":"({login_id}[^"]+)"', 'exa_regex=Subject:.+?Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:\s+({domain}.+?)\s+Logon ID:\s+({login_id}[^\s]+)'] |
| edit_regex_field | user |  | ['"SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)', 'exa_regex=Subject:.+?Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:\s+({domain}.+?)\s+Logon ID:\s+({login_id}[^\s]+)'] |
| added_attribute | ExtractionType |  | json |
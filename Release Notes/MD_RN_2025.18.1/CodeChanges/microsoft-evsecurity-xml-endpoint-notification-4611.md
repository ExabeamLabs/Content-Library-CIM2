# Code Changes for microsoft-evsecurity-xml-endpoint-notification-4611 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | auth_process |  | ['(\'|")LogonProcessName(\'|")>({auth_process}[^<"]+)<'] |
| edit_regex_field | domain |  | ['(\'|")SubjectDomainName(\'|")>({domain}[^"\s<]+)<'] |
| edit_regex_field | login_id |  | ['(\'|")SubjectLogonId(\'|")>({login_id}[^"\s<]+)<'] |
| edit_regex_field | user |  | ['(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<'] |
| edit_regex_field | user_sid |  | ['(\'|")SubjectUserSid(\'|")>({user_sid}[^"\s<]+)<'] |
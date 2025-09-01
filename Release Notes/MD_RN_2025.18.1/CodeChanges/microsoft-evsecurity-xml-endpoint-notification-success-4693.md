# Code Changes for microsoft-evsecurity-xml-endpoint-notification-success-4693 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)<\/Data>'] |
| edit_regex_field | result |  | ['<Data Name\\*=(\'|")FailureId(\'|")>({result}[^<]+)<\/Data>', '<Keywords>({result}[^<]+)<\/Keywords>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")SubjectUserSid(\'|")>({user_sid}[^<]+)<\/Data>'] |
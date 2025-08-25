# Code Changes for microsoft-evsecurity-xml-endpoint-notification-success-4802 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name=(\'|")TargetDomainName(\'|")>({domain}[^<]+)<\/Data'] |
| edit_regex_field | login_id |  | ['<Data Name=(\'|")TargetLogonId(\'|")>({login_id}[^<]+)<\/Data'] |
| edit_regex_field | user |  | ['<Data Name=(\'|")TargetUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data'] |
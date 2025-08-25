# Code Changes for microsoft-evsecurity-xml-group-member-add-success-eventid47 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | account_id |  | ['<Data Name=(\'|")MemberSid(\'|")>(({dest_user_sid}S-\d+\-[^<]+)|({account_id}[^<]+))<'] |
| edit_regex_field | dest_user_sid |  | ['<Data Name=(\'|")MemberSid(\'|")>(({dest_user_sid}S-\d+\-[^<]+)|({account_id}[^<]+))<'] |
| edit_regex_field | domain |  | ['<Data Name=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)<'] |
| edit_regex_field | login_id |  | ['<Data Name=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)<'] |
| edit_regex_field | user |  | ['<Data Name=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| edit_regex_field | user_sid |  | ['<Data Name=(\'|")SubjectUserSid(\'|")>({user_sid}[^<]+)<'] |
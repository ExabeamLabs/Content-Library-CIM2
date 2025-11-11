# Code Changes for microsoft-evsecurity-json-endpoint-logout-4647 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_host', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_id', 'result', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"TargetDomainName":"({dest_domain}({domain}[^"]+))"'] |
| edit_regex_field | host |  | ['"(Hostname|Computer)":"({dest_host}({host}[\w.-]+?))"'] |
| edit_regex_field | login_id |  | ['"TargetLogonId":"({dest_login_id}({login_id}[^"]+))"'] |
| edit_regex_field | user |  | ['"TargetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user_sid |  | ['"TargetUserSid":"({dest_user_sid}({user_sid}[^"]+))'] |
| added_regex_field | dest_domain |  | ['"TargetDomainName":"({dest_domain}({domain}[^"]+))"'] |
| added_regex_field | dest_host |  | ['"(Hostname|Computer)":"({dest_host}({host}[\w.-]+?))"'] |
| added_regex_field | dest_login_id |  | ['"TargetLogonId":"({dest_login_id}({login_id}[^"]+))"'] |
| added_regex_field | dest_user |  | ['"TargetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | dest_user_sid |  | ['"TargetUserSid":"({dest_user_sid}({user_sid}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for extremenetworks-zwlanm-str-endpoint-login-fail-loginfailed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'host', 'protocol', 'result', 'time', 'user'] |
| edit_regex_field | event_code |  | ["\s+({dest_host}({host}[^\s]+))\s+({event_code}%\d*SYSTEM-3-LOGIN_FAIL):\s+Log-in ({result}failed) for user '({user}[\w\.\-\!\#\^\~]{1,40}\$?)'\s+from '({protocol}[^']+)\'"] |
| edit_regex_field | host |  | ["\s+({dest_host}({host}[^\s]+))\s+({event_code}%\d*SYSTEM-3-LOGIN_FAIL):\s+Log-in ({result}failed) for user '({user}[\w\.\-\!\#\^\~]{1,40}\$?)'\s+from '({protocol}[^']+)\'"] |
| edit_regex_field | protocol |  | ["\s+({dest_host}({host}[^\s]+))\s+({event_code}%\d*SYSTEM-3-LOGIN_FAIL):\s+Log-in ({result}failed) for user '({user}[\w\.\-\!\#\^\~]{1,40}\$?)'\s+from '({protocol}[^']+)\'"] |
| edit_regex_field | result |  | ["\s+({dest_host}({host}[^\s]+))\s+({event_code}%\d*SYSTEM-3-LOGIN_FAIL):\s+Log-in ({result}failed) for user '({user}[\w\.\-\!\#\^\~]{1,40}\$?)'\s+from '({protocol}[^']+)\'"] |
| edit_regex_field | user |  | ["\s+({dest_host}({host}[^\s]+))\s+({event_code}%\d*SYSTEM-3-LOGIN_FAIL):\s+Log-in ({result}failed) for user '({user}[\w\.\-\!\#\^\~]{1,40}\$?)'\s+from '({protocol}[^']+)\'"] |
| added_regex_field | dest_host |  | ["\s+({dest_host}({host}[^\s]+))\s+({event_code}%\d*SYSTEM-3-LOGIN_FAIL):\s+Log-in ({result}failed) for user '({user}[\w\.\-\!\#\^\~]{1,40}\$?)'\s+from '({protocol}[^']+)\'"] |
| removed_attribute | DupFields |  | N/A |
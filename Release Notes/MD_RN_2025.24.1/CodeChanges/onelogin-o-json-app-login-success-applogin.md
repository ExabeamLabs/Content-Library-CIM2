# Code Changes for onelogin-o-json-app-login-success-applogin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_id', 'additional_info', 'app', 'failure_reason', 'full_name', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | user |  | ['"user_name":\s*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"'] |
| removed_attribute | DupFields |  | N/A |
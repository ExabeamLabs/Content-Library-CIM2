# Code Changes for onelogin-o-json-app-login-success-applogin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_id', 'additional_info', 'app', 'event_name', 'full_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | additional_info |  | ['"custom_message":\s*"({additional_info}[^",]+)"', '"error_description":\s*"({additional_info}[^\\",]+)"', '"notes":\s*"({additional_info}[^",]+)'] |
| edit_regex_field | app |  | ['"app_name":\s*"\s*({app}[^",]+)"'] |
| removed_regex_field | failure_reason |  | [] |
| edit_regex_field | full_name |  | ['"user_name":\s*"({full_name}[^\\",]+)"'] |
| added_regex_field | event_name |  | ['"event_type_name":\s*"({event_name}[^",]+)"'] |
| edit_attribute | activity_type |  | ['app-activity:success', 'app-login:fail', 'app-login:success', 'user-modify:success', 'user-password-reset:success'] |
| edit_attribute | legacy_activity_type |  | ['account-password-reset', 'app-activity', 'app-login', 'failed-app-login'] |
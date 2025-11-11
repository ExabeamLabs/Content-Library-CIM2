# Code Changes for cisco-asa-str-vpn-login-success-109005 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'src_ip', 'src_translated_ip', 'time', 'user'] |
| edit_regex_field | src_ip |  | ["Authentication succeeded for user '({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))' from ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}).+?to ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"] |
| edit_regex_field | src_translated_ip |  | ["Authentication succeeded for user '({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))' from ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}).+?to ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"] |
| edit_regex_field | user |  | ["Authentication succeeded for user '({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))' from ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}).+?to ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"] |
| added_regex_field | account |  | ["Authentication succeeded for user '({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))' from ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}).+?to ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"] |
| removed_attribute | DupFields |  | N/A |
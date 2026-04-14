# Code Changes for github-g-json-app-login-fail-failedlogin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'email_address', 'src_ip', 'src_user', 'user'] |
| added_regex_field | src_user |  | ['exa_json_path=$..actor,exa_regex=({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
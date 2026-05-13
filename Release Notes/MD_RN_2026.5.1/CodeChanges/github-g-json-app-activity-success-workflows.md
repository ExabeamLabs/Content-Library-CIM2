# Code Changes for github-g-json-app-activity-success-workflows (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'email_address', 'src_ip', 'src_user', 'user', 'user_type'] |
| edit_regex_field | user |  | ['exa_json_path=$..actor,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\[({user_type}[^\]"]+))?', 'exa_json_path=$..external_identity_nameid,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'exa_json_path=$..external_identity_username,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'exa_json_path=$..user,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\[({user_type}[^\]"]+))?'] |
| added_regex_field | user_type |  | ['exa_json_path=$..actor,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\[({user_type}[^\]"]+))?', 'exa_json_path=$..user,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\[({user_type}[^\]"]+))?'] |
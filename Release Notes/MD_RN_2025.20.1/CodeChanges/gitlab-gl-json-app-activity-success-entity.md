# Code Changes for gitlab-gl-json-app-activity-success-entity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['full_name', 'src_ip', 'src_port', 'user'] |
| edit_regex_field | user |  | ['exa_regex="author_name":"(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^",]+))"'] |
| added_regex_field | full_name |  | ['exa_regex="author_name":"(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^",]+))"'] |
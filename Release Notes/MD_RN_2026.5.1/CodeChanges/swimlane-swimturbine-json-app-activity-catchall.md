# Code Changes for swimlane-swimturbine-json-app-activity-catchall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'dest_user', 'email_address', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | dest_user |  | ['exa_regex=created a user with userName: ({dest_user}({account_name}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | email_address |  | ['exa_json_path=$.user,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user |  | ['exa_json_path=$.user,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | account_name |  | ['exa_regex=created a user with userName: ({dest_user}({account_name}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
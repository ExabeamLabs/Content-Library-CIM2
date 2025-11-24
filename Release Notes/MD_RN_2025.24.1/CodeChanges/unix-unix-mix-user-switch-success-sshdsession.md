# Code Changes for unix-unix-mix-user-switch-success-sshdsession (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_host', 'dest_ip', 'dest_user', 'dest_user_id', 'event_code', 'event_name', 'host', 'login_id', 'process_id', 'process_name', 'project_id', 'time', 'user', 'user_id', 'user_uid', 'zone'] |
| edit_regex_field | account |  | ['session opened for user ({dest_user}({account}.+?))(\(uid=({dest_user_id}\d+)\))? by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\(uid=({user_uid}({user_id}\d+))\)'] |
| edit_regex_field | dest_user_id |  | ['session opened for user ({dest_user}({account}.+?))(\(uid=({dest_user_id}\d+)\))? by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\(uid=({user_uid}({user_id}\d+))\)'] |
| edit_regex_field | user |  | ['session opened for user ({dest_user}({account}.+?))(\(uid=({dest_user_id}\d+)\))? by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\(uid=({user_uid}({user_id}\d+))\)'] |
| edit_regex_field | user_id |  | ['\(uid=({user_uid}({user_id}\d+))\)', 'session opened for user ({dest_user}({account}.+?))(\(uid=({dest_user_id}\d+)\))? by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\(uid=({user_uid}({user_id}\d+))\)'] |
| added_regex_field | dest_user |  | ['session opened for user ({dest_user}({account}.+?))(\(uid=({dest_user_id}\d+)\))? by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\(uid=({user_uid}({user_id}\d+))\)'] |
| added_regex_field | user_uid |  | ['\(uid=({user_uid}({user_id}\d+))\)', 'session opened for user ({dest_user}({account}.+?))(\(uid=({dest_user_id}\d+)\))? by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\(uid=({user_uid}({user_id}\d+))\)'] |
| removed_attribute | DupFields |  | N/A |
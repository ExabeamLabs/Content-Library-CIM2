# Code Changes for unix-unix-mix-user-switch-success-susession (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_host', 'dest_ip', 'dest_user', 'dest_user_id', 'event_code', 'event_name', 'host', 'process_id', 'process_name', 'time', 'user', 'user_id', 'user_uid'] |
| edit_regex_field | dest_user |  | ['({event_code}su):.+?for user ({account}({dest_user}[^\s]+?))(\(uid=({dest_user_id}\d+)\))? by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)?(\(uid=({user_id}({user_uid}\d+))\))?'] |
| edit_regex_field | dest_user_id |  | ['({event_code}su):.+?for user ({account}({dest_user}[^\s]+?))(\(uid=({dest_user_id}\d+)\))? by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)?(\(uid=({user_id}({user_uid}\d+))\))?'] |
| edit_regex_field | event_code |  | ['({event_code}su):.+?for user ({account}({dest_user}[^\s]+?))(\(uid=({dest_user_id}\d+)\))? by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)?(\(uid=({user_id}({user_uid}\d+))\))?'] |
| edit_regex_field | user |  | ['({event_code}su):.+?for user ({account}({dest_user}[^\s]+?))(\(uid=({dest_user_id}\d+)\))? by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)?(\(uid=({user_id}({user_uid}\d+))\))?'] |
| edit_regex_field | user_uid |  | ['({event_code}su):.+?for user ({account}({dest_user}[^\s]+?))(\(uid=({dest_user_id}\d+)\))? by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)?(\(uid=({user_id}({user_uid}\d+))\))?'] |
| added_regex_field | account |  | ['({event_code}su):.+?for user ({account}({dest_user}[^\s]+?))(\(uid=({dest_user_id}\d+)\))? by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)?(\(uid=({user_id}({user_uid}\d+))\))?'] |
| added_regex_field | user_id |  | ['({event_code}su):.+?for user ({account}({dest_user}[^\s]+?))(\(uid=({dest_user_id}\d+)\))? by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)?(\(uid=({user_id}({user_uid}\d+))\))?'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for unix-unix-str-user-switch-success-pam_unix (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['session opened for user \S+ by (({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|\(]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))?(\(uid\\?=({user_uid}({user_id}\d+))\))?'] |
| edit_regex_field | user |  | ['session opened for user ({dest_user}[^\s]+?)(\(uid=({dest_user_id}\d+)\))? by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)?(\(uid=({user_uid}\d+)\))?', 'session opened for user \S+ by (({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|\(]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))?(\(uid\\?=({user_uid}({user_id}\d+))\))?'] |
| edit_regex_field | user_id |  | ['session opened for user \S+ by (({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|\(]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))?(\(uid\\?=({user_uid}({user_id}\d+))\))?'] |
| edit_regex_field | user_uid |  | ['session opened for user ({dest_user}[^\s]+?)(\(uid=({dest_user_id}\d+)\))? by ({user}[\w\.\-\!\#\^\~]{1,40}\$?)?(\(uid=({user_uid}\d+)\))?', 'session opened for user \S+ by (({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|\(]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))?(\(uid\\?=({user_uid}({user_id}\d+))\))?'] |
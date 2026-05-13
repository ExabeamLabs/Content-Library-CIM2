# Code Changes for cisco-ios-kv-endpoint-notification-success-endpointnotification-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['Username entry \(((host\/({src_host}[\w.-]+))|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user_id}\d+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)\s'] |
| edit_regex_field | src_host |  | ['Username entry \(((host\/({src_host}[\w.-]+))|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user_id}\d+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)\s'] |
| edit_regex_field | user |  | ['Username entry \(((host\/({src_host}[\w.-]+))|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user_id}\d+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)\s'] |
| edit_regex_field | user_id |  | ['Username entry \(((host\/({src_host}[\w.-]+))|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user_id}\d+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)\s'] |
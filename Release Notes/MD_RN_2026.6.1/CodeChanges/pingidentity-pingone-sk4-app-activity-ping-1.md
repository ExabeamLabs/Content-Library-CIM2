# Code Changes for pingidentity-pingone-sk4-app-activity-ping-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"actors":\[\{"type":"user","name":"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | user |  | ['"actors":\[\{"type":"user","name":"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'suid=(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+=', 'suser=(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+='] |
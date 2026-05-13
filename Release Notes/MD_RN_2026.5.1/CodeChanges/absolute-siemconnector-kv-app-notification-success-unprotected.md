# Code Changes for absolute-siemconnector-kv-app-notification-success-unprotected (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['actorType=("Device".+?actorName="({src_host}[\w\-.]+)|"User".+?actorName="(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| edit_regex_field | src_host |  | ['actorType=("Device".+?actorName="({src_host}[\w\-.]+)|"User".+?actorName="(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| edit_regex_field | user |  | ['actorType=("Device".+?actorName="({src_host}[\w\-.]+)|"User".+?actorName="(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
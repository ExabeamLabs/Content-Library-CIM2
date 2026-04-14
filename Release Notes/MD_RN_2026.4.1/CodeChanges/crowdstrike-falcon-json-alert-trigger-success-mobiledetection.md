# Code Changes for crowdstrike-falcon-json-alert-trigger-success-mobiledetection (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"UserName":"*(({email_address}([A-Za-z0-9]+[!#$%&\'+\-\.\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))($|"|<)'] |
| edit_regex_field | user |  | ['"UserName":"*(({email_address}([A-Za-z0-9]+[!#$%&\'+\-\.\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))($|"|<)'] |
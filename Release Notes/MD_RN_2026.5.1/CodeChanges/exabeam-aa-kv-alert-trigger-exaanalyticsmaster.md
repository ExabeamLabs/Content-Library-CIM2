# Code Changes for exabeam-aa-kv-alert-trigger-exaanalyticsmaster (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\ssender="({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"', '\suser="\s*(\*+|(\w+-)?(\w+_)?\w+\.\.|(\w+?_)?(\w+-){1,2}\w+|((({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))))'] |
| edit_regex_field | user |  | ['\suser="\s*(\*+|(\w+-)?(\w+_)?\w+\.\.|(\w+?_)?(\w+-){1,2}\w+|((({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))))', 'user="({user}[\w\.\-\!\#\^\~]{1,40}\$?)"'] |
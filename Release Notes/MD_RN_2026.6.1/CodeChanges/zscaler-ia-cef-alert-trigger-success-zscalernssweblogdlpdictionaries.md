# Code Changes for zscaler-ia-cef-alert-trigger-success-zscalernssweblogdlpdictionaries (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\slogin=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)\s\w+=', '\ssuser=((noauth-protocol[^=]+)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)\s)|((\w+[^=]+\->\w+[^=]+)\s|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user |  | ['\ssuser=((noauth-protocol[^=]+)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)\s)|((\w+[^=]+\->\w+[^=]+)\s|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', '\ssuser=(NA|None|\$NULL|(\w+[^=]+\->\w+[^=]+)\s|(?![^\s]+@[^\s]+)({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\w+=|$)'] |
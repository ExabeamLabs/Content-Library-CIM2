# Code Changes for microsoft-o365-sk4-app-activity-success-pageviewed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\Wsuser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+(\w+=|$)', '\\?"+UserId\\?"+:\\?"+(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"+'] |
| edit_regex_field | user |  | ['\Wsuser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+(\w+=|$)', '\\?"+UserId\\?"+:\\?"+(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"+'] |
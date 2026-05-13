# Code Changes for microsoft-o365-sk4-app-activity-success-pageviewed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'auth_type', 'browser', 'correlation_id', 'email_address', 'event_subtype', 'object', 'operation', 'os', 'site_at', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| edit_regex_field | email_address |  | ['\Wsuser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+(\w+=|$)', '\\?"+UserId\\?"+:\\?"+(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"+'] |
| edit_regex_field | user |  | ['\Wsuser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+(\w+=|$)', '\\?"+UserId\\?"+:\\?"+(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"+'] |
| added_regex_field | site_at |  | ['"site":"({site_at}[^",]+)"'] |
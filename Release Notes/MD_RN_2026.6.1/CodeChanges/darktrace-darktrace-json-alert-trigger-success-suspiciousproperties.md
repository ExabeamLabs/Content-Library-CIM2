# Code Changes for darktrace-darktrace-json-alert-trigger-success-suspiciousproperties (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"key":\s*"Actor"[^\}]+?"values":\s*\[?"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\'\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | user |  | ['"key":\s*"Actor"[^\}]+?"values":\s*\[?"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\'\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
# Code Changes for github-g-json-app-activity-document_id (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"email":\s*"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+.[^\]\s"\\,\|]+)"', 'exa_json_path=$..email,exa_regex=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+.[^\]\s"\\,\|]+)', 'exa_json_path=$.external_identity_username,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user |  | ['"user":\s*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"', 'exa_json_path=$.external_identity_username,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
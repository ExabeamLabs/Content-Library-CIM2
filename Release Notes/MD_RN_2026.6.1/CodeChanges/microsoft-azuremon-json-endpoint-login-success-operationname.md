# Code Changes for microsoft-azuremon-json-endpoint-login-success-operationname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_json_path=$.identity.UserName,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| edit_regex_field | user |  | ['exa_json_path=$..user,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)', 'exa_json_path=$.identity.UserName,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
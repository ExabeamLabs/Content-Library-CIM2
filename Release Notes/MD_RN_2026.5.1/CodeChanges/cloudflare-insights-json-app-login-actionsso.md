# Code Changes for cloudflare-insights-json-app-login-actionsso (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_json_path=$.Email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+.[^\]\s"\\,\|]+)'] |
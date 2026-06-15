# Code Changes for cloudflare-insights-json-app-activity-actiontype (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_json_path=$..ActorEmail,exa_regex=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+.[^\]\s"\\,\|]+)'] |
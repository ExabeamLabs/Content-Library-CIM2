# Code Changes for microsoft-azuremon-sk4-app-activity-auditevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_regex=identity\/claims\/name":"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)'] |
| edit_regex_field | full_name |  | ['exa_regex="idtyp":"user"[^\}]+"name":"({full_name}[^"]+)'] |
# Code Changes for microsoft-o365-sk4-app-activity-success-softdelete (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | user_agent | ['"ClientInfoString":"({user_agent}[^"]+)",', '"userAgent":"({user_agent}[^"]+)"'] | ['"ActorInfoString":"({user_agent}[^"]+)",', '"ClientInfoString":"({user_agent}[^"]+)",', '"userAgent":"({user_agent}[^"]+)"'] |
# Code Changes for cef-microsoft-app-activity-2 (ParserTemplate)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | user_agent | ['"(?i)userAgent":"({user_agent}[^"]+)"', '"ClientInfoString":"({user_agent}[^"]+)",'] | ['"(?i)userAgent":"({user_agent}[^"]+)"', '"ActorInfoString":"({user_agent}[^"]+)",', '"ClientInfoString":"({user_agent}[^"]+)",'] |
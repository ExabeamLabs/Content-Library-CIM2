# Code Changes for microsoft-azuremon-sk4-app-logout-sshlogout (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | user_agent | ['"(?i)userAgent":"({user_agent}[^"]+)"', '"ClientInfoString":"({user_agent}[^"]+)",'] | ['"(?i)userAgent":"({user_agent}[^"]+)"', '"ActorInfoString":"({user_agent}[^"]+)",', '"ClientInfoString":"({user_agent}[^"]+)",'] |
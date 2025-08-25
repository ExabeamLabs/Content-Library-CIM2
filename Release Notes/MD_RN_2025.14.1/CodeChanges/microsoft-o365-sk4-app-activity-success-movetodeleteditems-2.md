# Code Changes for microsoft-o365-sk4-app-activity-success-movetodeleteditems-2 (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | user_agent | ['"ClientInfoString":\s*"({user_agent}[^"]+)",'] | ['"ActorInfoString":\s*"({user_agent}[^"]+)",', '"ClientInfoString":\s*"({user_agent}[^"]+)",'] |
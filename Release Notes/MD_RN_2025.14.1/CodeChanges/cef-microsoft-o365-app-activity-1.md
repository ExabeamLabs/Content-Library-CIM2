# Code Changes for cef-microsoft-o365-app-activity-1 (ParserTemplate)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | user_agent | ['"ClientInfoString":\s*"({user_agent}[^"]+)",'] | ['"ActorInfoString":\s*"({user_agent}[^"]+)",', '"ClientInfoString":\s*"({user_agent}[^"]+)",'] |
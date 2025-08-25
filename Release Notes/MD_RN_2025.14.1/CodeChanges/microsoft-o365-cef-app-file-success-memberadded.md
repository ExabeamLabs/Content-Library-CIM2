# Code Changes for microsoft-o365-cef-app-file-success-memberadded (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | user_agent | ['"ClientInfoString":\s*"({user_agent}[^"]+)",', '"User-Agent\\?"+:\\?"+({user_agent}[^"\\]+)', '"UserAgent":\s*"({user_agent}[^"]+)"', '("key":\s*"User-Agent","value":\s*"({user_agent}[^"]+?)"|"value":"({=user_agent}[^"]+?)","key":"User-Agent")'] | ['"ActorInfoString":\s*"({user_agent}[^"]+)",', '"ClientInfoString":\s*"({user_agent}[^"]+)",', '"User-Agent\\?"+:\\?"+({user_agent}[^"\\]+)', '"UserAgent":\s*"({user_agent}[^"]+)"', '("key":\s*"User-Agent","value":\s*"({user_agent}[^"]+?)"|"value":"({=user_agent}[^"]+?)","key":"User-Agent")'] |
# Code Changes for microsoft-copilot-json-ai-agent-request-success-interaction-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'action', 'ai_tool_name', 'app', 'app_type', 'blocked', 'conversation_id', 'email_address', 'email_domain', 'event_name', 'full_name', 'message_id', 'model_name', 'resource_id', 'resource_name', 'resource_type', 'src_ip', 'src_port', 'time', 'url', 'user', 'user_type'] |
| edit_regex_field | access |  | ['"Action"\s*:\s*"({action}({access}[^",]+))"', '"Action"\s*:\s*"({action}({access}[^",]+))"'] |
| edit_regex_field | email_address |  | ['"UserId"\s*:\s*"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_json_path=$..UserId,exa_regex=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_domain |  | ['"UserId"\s*:\s*"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_json_path=$..UserId,exa_regex=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | user |  | ['"UserId"\s*:\s*"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | action |  | ['"Action"\s*:\s*"({action}({access}[^",]+))"', '"Action"\s*:\s*"({action}({access}[^",]+))"'] |
| added_regex_field | ai_tool_name |  | ['"AISystemPlugin"\s*:.+?"Name"\s*:\s*"({ai_tool_name}[^"]+)"'] |
| added_regex_field | blocked |  | ['"JailbreakDetected"\s*:\s*({blocked}true|false)'] |
| added_regex_field | conversation_id |  | ['"ThreadId"\s*:\s*"({conversation_id}[^"]+)"'] |
| added_regex_field | message_id |  | ['"Messages"\s*:\s*.+?"Id"\s*:\s*"({message_id}[^"]+)"'] |
| added_regex_field | model_name |  | ['"ModelName"\s*:\s*"({model_name}[^"]+)"'] |
| added_regex_field | resource_id |  | ['"AccessedResources"\s*:\s*.+?"Id"\s*:\s*"({resource_id}[^"]+)"'] |
| added_regex_field | resource_name |  | ['"AccessedResources"\s*:\s*.+?"Name"\s*:\s*"({resource_name}[^"]+)"'] |
| added_regex_field | resource_type |  | ['"AccessedResources"\s*:\s*.+?"Type"\s*:\s*"({resource_type}[^"]+)"'] |
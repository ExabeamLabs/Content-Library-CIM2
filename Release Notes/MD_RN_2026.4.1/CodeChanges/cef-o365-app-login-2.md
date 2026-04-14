# Code Changes for cef-o365-app-login-2 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'event_name', 'host', 'result', 'src_ip', 'src_port', 'time', 'user_agent', 'user_upn'] |
| added_regex_field | host |  | ['"DeviceProperties":.+?"DisplayName",\s*"Value":\s*"({host}[\w\-.]+)"'] |
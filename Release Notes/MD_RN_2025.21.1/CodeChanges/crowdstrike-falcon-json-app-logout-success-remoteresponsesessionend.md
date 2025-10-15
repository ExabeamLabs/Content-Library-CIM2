# Code Changes for crowdstrike-falcon-json-app-logout-success-remoteresponsesessionend (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | operation |  | ['"(?i)EventType":\s*"({operation}[^",]+)"', '"ExternalApiType":\s*"({operation}[^"]+)"'] |
| removed_attribute | DupFields |  | N/A |
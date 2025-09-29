# Code Changes for crowdstrike-falcon-json-alert-trigger-success-identityprotection (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['"EndpointName":\s*"({host}[\w\-.]+)"', 'exa_json_path=$.event.EndpointName,exa_regex=^({host}[\w\-.]+)$'] |
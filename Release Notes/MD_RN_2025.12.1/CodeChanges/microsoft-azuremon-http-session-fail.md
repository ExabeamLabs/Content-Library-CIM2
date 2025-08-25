# Code Changes for microsoft-azuremon-http-session-fail (Event Builder)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_conditions | expression | InList(type, 'microsoft-azuremon-json-http-session-requestmethod') && exists(http_response_code) && !StartsWithAny(http_response_code,'1','2','3') | InList(type, 'microsoft-azuremon-json-http-session-requestmethod') && !StartsWithAny(http_response_code,'1','2','3') |
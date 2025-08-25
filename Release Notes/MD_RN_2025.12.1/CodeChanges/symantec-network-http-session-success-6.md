# Code Changes for symantec-network-http-session-success-6 (Event Builder)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_conditions | expression | InList(type, 'symantec-fireglass-cef-http-session-isolation') and !InList(ToLower(action), 'block') and (!exists(http_response_code) or (exists(http_response_code) && StartsWithAny(http_response_code,'1','2','3'))) | InList(type, 'symantec-fireglass-cef-http-session-isolation') and !InList(ToLower(action), 'block')  && StartsWithAny(http_response_code,'1','2','3') |
# Code Changes for microsoft-azure-secret-read-success (Event Builder)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_conditions | expression | InList(type, 'microsoft-azure-json-key-success-keyvault', 'microsoft-azuremon-sk4-app-activity-auditevent') && InList(toLower(operation), 'secretget','secretlist', 'secretgetdeleted', 'secretlistdeleted') && (!exists(http_response_code) || !startsWithAny(http_response_code,'4', '5', '6')) | InList(type, 'microsoft-azure-json-key-success-keyvault', 'microsoft-azuremon-sk4-app-activity-auditevent') && InList(toLower(operation), 'secretget','secretlist', 'secretgetdeleted', 'secretlistdeleted') && !startsWithAny(http_response_code,'4', '5', '6') |
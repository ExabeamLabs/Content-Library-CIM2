# Code Changes for cisco-cucm-kv-endpoint-authentication-fail-userlogging (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| changed | Conditions | ['=Login Authentication Failed]', 'EventType =UserLogging'] | ['%UC_AUDITLOG-', '=Login Authentication Failed]', '=UserLogging', 'EventType'] |
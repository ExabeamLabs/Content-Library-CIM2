# Code Changes for cisco-cucm-kv-endpoint-login-success-authsuccess (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| changed | Conditions | ['=Login Authentication Successful]', 'EventType =UserLogging'] | [' %UC_AUDITLOG-', '=Login Authentication Successful]', '=UserLogging', 'EventType'] |
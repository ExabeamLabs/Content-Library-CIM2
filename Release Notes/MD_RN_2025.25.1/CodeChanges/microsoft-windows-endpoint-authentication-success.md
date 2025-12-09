# Code Changes for microsoft-windows-endpoint-authentication-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-evsecurity-json-endpoint-kerberosauth','microsoft-evsecurity-json-endpoint-mcafeeesm') and exists(result_code) and InList(toLower(result_code), '0x0', '-', 'success', 'accept', 'the operation completed successfully') |
# Code Changes for dl-microsoft-windows-endpoint-login-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type , 'microsoft-defenderep-kv-endpoint-login-devicelogonevents','microsoft-evsystem-kv-endpoint-login-success-7001','microsoft-evsystem-str-endpoint-login-success-7001') |
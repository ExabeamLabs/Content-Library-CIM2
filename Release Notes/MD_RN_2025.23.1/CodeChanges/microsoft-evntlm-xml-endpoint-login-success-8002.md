# Code Changes for microsoft-evntlm-xml-endpoint-login-success-8002 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"] |
| changed | Conditions |  | ['<Channel>Microsoft-Windows-NTLM/Operational<', '<EventID>8002<', '<Provider Name='] |
| edit_attribute | activity_type |  | ['endpoint-activity:success'] |
| edit_attribute | legacy_activity_type |  | ['app-activity'] |
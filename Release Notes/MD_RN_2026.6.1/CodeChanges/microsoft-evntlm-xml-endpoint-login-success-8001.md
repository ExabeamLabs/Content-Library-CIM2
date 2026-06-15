# Code Changes for microsoft-evntlm-xml-endpoint-login-success-8001 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"] |
| changed | Conditions |  | ['<Channel>Microsoft-Windows-NTLM/Operational<', '<EventID>8001<', '<Provider Name='] |
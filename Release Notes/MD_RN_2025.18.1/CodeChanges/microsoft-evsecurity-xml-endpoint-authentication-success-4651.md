# Code Changes for microsoft-evsecurity-xml-endpoint-authentication-success-4651 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | ['<Data Name\\*=(\'|")RemoteMMPrincipalName(\'|")>({dest_host}[\w\-.]+)'] |
| edit_regex_field | src_host |  | ['<Data Name\\*=(\'|")LocalMMPrincipalName(\'|")>({src_host}[^<]+)'] |
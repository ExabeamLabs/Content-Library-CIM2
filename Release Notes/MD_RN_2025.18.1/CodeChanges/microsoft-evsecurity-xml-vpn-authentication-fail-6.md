# Code Changes for microsoft-evsecurity-xml-vpn-authentication-fail-6 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | account |  | ['<Data Name\\*=(\'|")Context(\'|")>({account}[^<]+?)</Data>'] |
| edit_regex_field | failure_reason |  | ['<Data Name\\*=(\'|")ErrorCode(\'|")>({failure_reason}[^<]+?)</Data>', '<Data Name\\*=(\'|")ErrorDescription(\'|")>({failure_reason}[^<]+?)\s*</Data>'] |
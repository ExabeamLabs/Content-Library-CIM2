# Code Changes for microsoft-evapp-xml-certificate-request-fail-49754 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | additional_info |  | ['<Data Name\\*=(\'|")RequestId(\'|")>({additional_info}({src_host}[^<\\]+)\\+({domain}\w+)[^<]*?)</Data>'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")RequestId(\'|")>({additional_info}({src_host}[^<\\]+)\\+({domain}\w+)[^<]*?)</Data>', 'Account Domain:\s*(NT AUTHORITY|({domain}\S+))\s+Logon ID:'] |
| edit_regex_field | host_type |  | ['<Data Name\\*=(\'|")TemplateName(\'|")>({host_type}[^<]+?)</Data>'] |
| edit_regex_field | src_host |  | ['<Data Name\\*=(\'|")RequestId(\'|")>({additional_info}({src_host}[^<\\]+)\\+({domain}\w+)[^<]*?)</Data>'] |
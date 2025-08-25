# Code Changes for microsoft-evsecurity-xml-dns-record-create-fail-8015 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | failure_code |  | ['<Data Name=(\'|")ErrorCode(\'|")>({failure_code}[^<]+)<\/Data>'] |
# Code Changes for microsoft-sysmon-xml-dll-load-7 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | hash_md5 |  | ['<Data Name\\*=(\'|")Hash(es)?(\'|")>[^<>]*?MD5=({hash_md5}[^,<]+)'] |
| edit_regex_field | signature |  | ['<Data Name\\*=(\'|")Signature(\'|")>({signature}[^<>]+?)<\/Data>'] |
| edit_regex_field | signed |  | ['<Data Name\\*=(\'|")Signed(\'|")>({signed}[^<>]+?)<\/Data>'] |
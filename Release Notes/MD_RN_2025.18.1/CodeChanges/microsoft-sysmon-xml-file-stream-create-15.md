# Code Changes for microsoft-sysmon-xml-file-stream-create-15 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | hash_md5 |  | ['<Data Name\\*=(\'|")Hashes(\'|")>MD5=({hash_md5}[^,]+)'] |
# Code Changes for microsoft-evsecurity-xml-ds-object-restore-success-5138 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | correlation_id |  | ['<Data Name\\*=(\'|")OpCorrelationID(\'|")>\{({correlation_id}[^\}<]+)\}<'] |
| edit_regex_field | object_id |  | ['<Data Name\\*=(\'|")ObjectGUID(\'|")>\{({object_id}[^<\}]+)\}<'] |
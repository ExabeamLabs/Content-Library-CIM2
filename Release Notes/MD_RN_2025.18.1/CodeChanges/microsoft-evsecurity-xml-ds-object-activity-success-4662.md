# Code Changes for microsoft-evsecurity-xml-ds-object-activity-success-4662 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | access |  | ['<Data Name\\*=(\'|")AccessList(\'|")>(-|({access}[^<]+?))\s*<', 'Accesses:\s*(-|({access}[^:]+?))\s+Access Mask:'] |
| edit_regex_field | access_list |  | ['<Data Name\\*=(\'|")AccessList(\'|")>(-|({access_list}[^<]+?))\s*<'] |
| edit_regex_field | access_mask |  | ['<Data Name\\*=(\'|")AccessMask(\'|")>(-|({access_mask}[^<]+?))\s*<'] |
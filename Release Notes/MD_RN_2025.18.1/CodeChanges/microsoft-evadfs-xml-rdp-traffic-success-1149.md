# Code Changes for microsoft-evadfs-xml-rdp-traffic-success-1149 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}[^\'"]+)(\'|")'] |
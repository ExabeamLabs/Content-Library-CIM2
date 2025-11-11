# Code Changes for hp-arubacpm-leef-app-login-success-loggedin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | operation |  | ['action=(None|({operation}[^=]+?))\s+\w+?=', 'sub-cat=({operation}[^=]+?)\s+\w+?='] |
| removed_attribute | DupFields |  | N/A |
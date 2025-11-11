# Code Changes for cisco-ise-cef-radius-traffic-success-cisepassedauth (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | auth_server |  | ['dhost=({auth_server}[^\s]+)', 'dst=({auth_server}[A-Fa-f:\d.]+)\s', 'dvchost=({auth_server}[^\s]+)'] |
| removed_attribute | DupFields |  | N/A |
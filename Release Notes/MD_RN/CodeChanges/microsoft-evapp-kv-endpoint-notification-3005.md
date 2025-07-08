# Code Changes for microsoft-evapp-kv-endpoint-notification-3005 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_name | ['Process name:\s+({process_name}[^=]+?)\s+Account name:', 'exa_regex=Process name:\s+({process_name}[^=]+?)\s+Account name:'] | ['Process name:\s+({process_name}[^=]+?)(\s|\\[rnt])+Account name:', 'exa_regex=Process name:\s+({process_name}[^=]+?)(\s|\\[rnt])+Account name:'] |
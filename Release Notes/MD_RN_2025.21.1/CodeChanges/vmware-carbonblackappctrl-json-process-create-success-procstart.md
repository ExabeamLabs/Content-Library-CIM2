# Code Changes for vmware-carbonblackappctrl-json-process-create-success-procstart (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | parent_process_command_line |  | ['"+parent_cmdline"+:"+({parent_process_command_line}.+?)\s*(",\s*"|"\s*})'] |
| edit_regex_field | process_command_line |  | ['"+process_cmdline"+:"+({process_command_line}.+?)\s*(",\s*"|"\s*})'] |
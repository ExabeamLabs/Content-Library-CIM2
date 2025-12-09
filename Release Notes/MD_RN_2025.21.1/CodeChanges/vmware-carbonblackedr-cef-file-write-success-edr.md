# Code Changes for vmware-carbonblackedr-cef-file-write-success-edr (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | parent_process_command_line |  | ['"+parent_cmdline"+:"+\s*({parent_process_command_line}.+?)\s*(",\s*"|"\s*})'] |
| edit_regex_field | process_command_line |  | ['"+process_cmdline"+:"+\s*({process_command_line}.+?)\s*(",\s*"|"\s*})'] |
# Code Changes for unix-ad-kv-process-create-success-audispd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['exe="({process_dir}.*\/)({process_name}[^"]+?)"\s*\w+='] |
| edit_regex_field | process_name |  | ['exe="({process_dir}.*\/)({process_name}[^"]+?)"\s*\w+='] |
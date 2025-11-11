# Code Changes for microsoft-azure-json-process-create-success-vmprocess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['\"ExecutablePath\":\"({process_path}((|({process_dir}[^\"]*?)[\\/]+))?({process_name}[^\"\\/]+?))\s*\"'] |
| edit_regex_field | process_name |  | ['ExecutableName\"+:\"+({process_name}[^\"]+)', '\"ExecutablePath\":\"({process_path}((|({process_dir}[^\"]*?)[\\/]+))?({process_name}[^\"\\/]+?))\s*\"'] |
| edit_regex_field | process_path |  | ['\"ExecutablePath\":\"({process_path}((|({process_dir}[^\"]*?)[\\/]+))?({process_name}[^\"\\/]+?))\s*\"'] |
| removed_attribute | DupFields |  | N/A |
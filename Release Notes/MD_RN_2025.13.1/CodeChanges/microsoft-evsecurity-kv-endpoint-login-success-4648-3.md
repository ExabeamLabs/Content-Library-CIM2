# Code Changes for microsoft-evsecurity-kv-endpoint-login-success-4648-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['Process Name(:|=)\s*(\\r|\\t|\\n)*(-|({process_path}({process_dir}\w:([^:=]+)?[\\\/])?\s*(|({process_name}[^\\\/;\s]+\.\w+))))(;|\s|\\[rnt]|\s)+'] |
| edit_regex_field | process_name |  | ['Process Name(:|=)\s*(\\r|\\t|\\n)*(-|({process_path}({process_dir}\w:([^:=]+)?[\\\/])?\s*(|({process_name}[^\\\/;\s]+\.\w+))))(;|\s|\\[rnt]|\s)+'] |
| edit_regex_field | process_path |  | ['Process Name(:|=)\s*(\\r|\\t|\\n)*(-|({process_path}({process_dir}\w:([^:=]+)?[\\\/])?\s*(|({process_name}[^\\\/;\s]+\.\w+))))(;|\s|\\[rnt]|\s)+'] |
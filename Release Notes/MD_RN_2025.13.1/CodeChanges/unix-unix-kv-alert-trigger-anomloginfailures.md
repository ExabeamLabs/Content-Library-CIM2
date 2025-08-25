# Code Changes for unix-unix-kv-alert-trigger-anomloginfailures (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['\sexe="({process_dir}[^"]+[\/\\])({process_name}[^"\\\/]+?)"'] |
| edit_regex_field | process_name |  | ['\sexe="({process_dir}[^"]+[\/\\])({process_name}[^"\\\/]+?)"'] |
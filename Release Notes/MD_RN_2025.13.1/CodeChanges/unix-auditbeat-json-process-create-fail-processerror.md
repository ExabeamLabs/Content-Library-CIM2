# Code Changes for unix-auditbeat-json-process-create-fail-processerror (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['"process".+?"executable":"({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+?))"'] |
| edit_regex_field | process_name |  | ['"process".+?"executable":"({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+?))"', '"process":.+?"name":"({process_name}[^"]+)"'] |
| edit_regex_field | process_path |  | ['"process".+?"executable":"({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+?))"'] |
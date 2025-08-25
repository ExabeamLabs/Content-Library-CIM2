# Code Changes for unix-unix-kv-service-stop-success-servicestop (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | process_dir | ['\sexe="({process_path}({process_dir}[^"]+?)\/[^"\\\/]+)"'] | ['\sa0="({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^"]+?))"', '\sexe="({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^"]+?))"'] |
| edit_regex_field | process_name | ['\sa0="({process_name}[^"]+)"', '\scomm="({process_name}[^\\"]+)"'] | ['\sa0="({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^"]+?))"', '\scomm="({process_name}[^\\"]+)"', '\sexe="({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^"]+?))"'] |
| edit_regex_field | process_path | ['\sexe="({process_path}({process_dir}[^"]+?)\/[^"\\\/]+)"'] | ['\sa0="({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^"]+?))"', '\sexe="({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^"]+?))"'] |
| changed | Conditions | ['exe=', 'msg=audit(', 'res=', 'type=SERVICE_STOP'] | ['SERVICE_STOP', 'audit', 'exe=', 'msg=', 'res='] |
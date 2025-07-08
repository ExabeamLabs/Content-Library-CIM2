# Code Changes for unix-unix-kv-endpoint-activity-success-bprmfcaps (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir | ['\sexe="({process_path}({process_dir}[^"]+?)\/[^"\\\/]+)"'] | ['\sa0="({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^"]+?))"', '\sexe="({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^"]+?))"'] |
| edit_regex_field | process_name | ['\sa0="({process_name}[^"]+)"', '\scomm="({process_name}[^\\"]+)"'] | ['\sa0="({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^"]+?))"', '\scomm="({process_name}[^\\"]+)"', '\sexe="({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^"]+?))"'] |
| edit_regex_field | process_path | ['\sexe="({process_path}({process_dir}[^"]+?)\/[^"\\\/]+)"'] | ['\sa0="({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^"]+?))"', '\sexe="({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^"]+?))"'] |
| changed | Conditions | ['msg=audit(', 'type=BPRM_FCAPS'] | ['BPRM_FCAPS', 'audit', 'msg='] |
# Code Changes for microsoft-evsecurity-kv-endpoint-login-success-successfullyloggedon (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_domain', 'dest_host', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'key_length', 'login_id', 'login_type', 'process_dir', 'process_name', 'process_path', 'src_host', 'src_host_windows', 'src_ip', 'subject_sid', 'time', 'user', 'user_sid', 'user_upn'] |
| edit_regex_field | domain |  | ['New Logon(:|=)[^\}]*?Account Domain(:|=)\s*(-|({dest_domain}({domain}[^\s]+?)))[\s;]*Logon ID(:|=)'] |
| edit_regex_field | src_host_windows |  | ['Workstation Name(:|=)\s*(-|[A-Fa-f:\d.]+|(?:\\+)?({src_host_windows}({src_host}[\w.\-]+\$?)))[\s;]*Source Network Address(:|=)'] |
| edit_regex_field | user |  | ['New Logon(:|=)[\s;]*Security ID(:|=)[^\}:]*?Account Name(:|=)\s*(-|SYSTEM|(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))[\s;]*Account Domain(:|=)'] |
| edit_regex_field | user_sid |  | ['New Logon(:|=)[\s;]*Security ID(:|=)\s*(NT AUTHORITY\\+SYSTEM|({dest_user_sid}({user_sid}[^;:=]+?)))(\s+|;)Account Name(:|=)'] |
| edit_regex_field | user_upn |  | ['New Logon(:|=)[\s;]*Security ID(:|=)[^\}:]*?Account Name(:|=)\s*(-|SYSTEM|(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))[\s;]*Account Domain(:|=)'] |
| added_regex_field | dest_domain |  | ['New Logon(:|=)[^\}]*?Account Domain(:|=)\s*(-|({dest_domain}({domain}[^\s]+?)))[\s;]*Logon ID(:|=)'] |
| added_regex_field | dest_user |  | ['New Logon(:|=)[\s;]*Security ID(:|=)[^\}:]*?Account Name(:|=)\s*(-|SYSTEM|(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))[\s;]*Account Domain(:|=)'] |
| added_regex_field | dest_user_sid |  | ['New Logon(:|=)[\s;]*Security ID(:|=)\s*(NT AUTHORITY\\+SYSTEM|({dest_user_sid}({user_sid}[^;:=]+?)))(\s+|;)Account Name(:|=)'] |
| added_regex_field | src_host |  | ['Workstation Name(:|=)\s*(-|[A-Fa-f:\d.]+|(?:\\+)?({src_host_windows}({src_host}[\w.\-]+\$?)))[\s;]*Source Network Address(:|=)'] |
| removed_attribute | DupFields |  | N/A |
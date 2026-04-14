# Code Changes for microsoft-evsecurity-kv-endpoint-login-success-successfullyloggedon (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | auth_package |  | ['Logon Process(:|=)\s*(\\t|\\r|\\n)*({auth_process}[^\s;]+?)[\s;]*(\\t|\\r|\\n)*Authentication Package(:|=)\s*(\\t|\\r|\\n)*({auth_package}[^\s;\\]+)'] |
| edit_regex_field | auth_process |  | ['Logon Process(:|=)\s*(\\t|\\r|\\n)*({auth_process}[^\s;]+?)[\s;]*(\\t|\\r|\\n)*Authentication Package(:|=)\s*(\\t|\\r|\\n)*({auth_package}[^\s;\\]+)'] |
| edit_regex_field | dest_domain |  | ['New Logon(:|=)[^\}]*?Account Domain(:|=)\s*(\\t|\\r|\\n)*(-|({dest_domain}({domain}[^\s]+?)))[\s;]*(\\t|\\r|\\n)*Logon ID(:|=)'] |
| edit_regex_field | dest_login_id |  | ['Linked Logon ID:\s*(\\t|\\r|\\n)*({dest_login_id}[^\s\\]+)'] |
| edit_regex_field | dest_user |  | ['New Logon(:|=)[\s;]*(\\t|\\r|\\n)*Security ID(:|=)[^\}:]*?Account Name(:|=)\s*(\\t|\\r|\\n)*(-|SYSTEM|(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))[\s;]*(\\t|\\r|\\n)*Account Domain(:|=)'] |
| edit_regex_field | dest_user_sid |  | ['New Logon(:|=)[\s;]*(\\t|\\r|\\n)*Security ID(:|=)\s*(\\t|\\r|\\n)*(NT AUTHORITY\\+SYSTEM|({dest_user_sid}({user_sid}[^;:=]+?)))[\s;]*(\\t|\\r|\\n)*Account Name(:|=)'] |
| edit_regex_field | domain |  | ['New Logon(:|=)[^\}]*?Account Domain(:|=)\s*(\\t|\\r|\\n)*(-|({dest_domain}({domain}[^\s]+?)))[\s;]*(\\t|\\r|\\n)*Logon ID(:|=)'] |
| edit_regex_field | key_length |  | ['Key Length(:|=)\s*(\\t|\\r|\\n)*({key_length}\d+)'] |
| edit_regex_field | login_id |  | ['Logon ID(:|=)\s*(\\t|\\r|\\n)*({login_id}[^\s;]+?)[\s;]*(\\t|\\r|\\n)*(Linked Logon|Logon GUID)'] |
| edit_regex_field | login_type |  | ['Logon Type(:|=)\s*(\\t|\\r|\\n)*({login_type}\d+)'] |
| edit_regex_field | process_dir |  | ['Process Name(:|=)\s*(\\t|\\r|\\n)*(?:-|({process_path}({process_dir}[^\}]*?)(\\+({process_name}[^\\]+?))?))\s*(\\t|\\r|\\n)*(Network Information:|Additional Information:)'] |
| edit_regex_field | process_name |  | ['Process Name(:|=)\s*(\\t|\\r|\\n)*(?:-|({process_path}({process_dir}[^\}]*?)(\\+({process_name}[^\\]+?))?))\s*(\\t|\\r|\\n)*(Network Information:|Additional Information:)'] |
| edit_regex_field | process_path |  | ['Process Name(:|=)\s*(\\t|\\r|\\n)*(?:-|({process_path}({process_dir}[^\}]*?)(\\+({process_name}[^\\]+?))?))\s*(\\t|\\r|\\n)*(Network Information:|Additional Information:)'] |
| edit_regex_field | src_host |  | ['Workstation Name(:|=)\s*(\\t|\\r|\\n)*(-|[A-Fa-f:\d.]+|(?:\\+)?({src_host_windows}({src_host}[\w.\-]+\$?)))[\s;]*(\\t|\\r|\\n)*Source Network Address(:|=)'] |
| edit_regex_field | src_host_windows |  | ['Workstation Name(:|=)\s*(\\t|\\r|\\n)*(-|[A-Fa-f:\d.]+|(?:\\+)?({src_host_windows}({src_host}[\w.\-]+\$?)))[\s;]*(\\t|\\r|\\n)*Source Network Address(:|=)'] |
| edit_regex_field | src_ip |  | ['Source Network Address(:|=)\s*(\\t|\\r|\\n)*(?:-|({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f\d]+:[A-Fa-f\d:]+)))[\s;]*(\\t|\\r|\\n)*Source Port(:|=)'] |
| edit_regex_field | subject_sid |  | ['Subject(:|=)[\s;]*(\\t|\\r|\\n)*Security ID(:|=)\s*(\\t|\\r|\\n)*({subject_sid}[^;:=]+?)[\s+;]*(\\t|\\r|\\n)*Account Name(:|=)'] |
| edit_regex_field | user |  | ['New Logon(:|=)[\s;]*(\\t|\\r|\\n)*Security ID(:|=)[^\}:]*?Account Name(:|=)\s*(\\t|\\r|\\n)*(-|SYSTEM|(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))[\s;]*(\\t|\\r|\\n)*Account Domain(:|=)'] |
| edit_regex_field | user_sid |  | ['New Logon(:|=)[\s;]*(\\t|\\r|\\n)*Security ID(:|=)\s*(\\t|\\r|\\n)*(NT AUTHORITY\\+SYSTEM|({dest_user_sid}({user_sid}[^;:=]+?)))[\s;]*(\\t|\\r|\\n)*Account Name(:|=)'] |
| edit_regex_field | user_upn |  | ['New Logon(:|=)[\s;]*(\\t|\\r|\\n)*Security ID(:|=)[^\}:]*?Account Name(:|=)\s*(\\t|\\r|\\n)*(-|SYSTEM|(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))[\s;]*(\\t|\\r|\\n)*Account Domain(:|=)'] |
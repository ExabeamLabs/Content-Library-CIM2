# Code Changes for microsoft-evsecurity-json-endpoint-4624 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_domain', 'dest_host', 'dest_user', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'login_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_mac', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['New Logon[\s\S]*?Account Domain(:|=)\s*(-|({dest_domain}({domain}[^\s]+?)))[\s;]*Logon ID(:|=)', 'TargetDomainName\\?"+:\\?"({dest_domain}({domain}[^\s",\\]+))\\?"'] |
| edit_regex_field | host |  | ['"(?:winlog\.)?computer_name\\*":\\*"({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | src_host_windows |  | ['Workstation Name(:|=)\s*((?-i)\\+[rnt])*(-|[A-Fa-f:\d.]+|({src_host_windows}({src_host}[\w\-\.]+)))[\s;]*((?-i)\\+[rnt])*Source Network Address(:|=)', 'WorkstationName\\?"+:\\?"+(?:-|({src_host_windows}({src_host}[\w\-\.]+)))\\?"'] |
| edit_regex_field | user |  | ['New Logon[\s\S]*?Account Name(:|=)\s*(-|SYSTEM|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))[\s;]*Account Domain(:|=)', 'TargetUserName\\?"+:\\?"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"'] |
| added_regex_field | dest_domain |  | ['New Logon[\s\S]*?Account Domain(:|=)\s*(-|({dest_domain}({domain}[^\s]+?)))[\s;]*Logon ID(:|=)', 'TargetDomainName\\?"+:\\?"({dest_domain}({domain}[^\s",\\]+))\\?"'] |
| added_regex_field | dest_host |  | ['"(?:winlog\.)?computer_name\\*":\\*"({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_user |  | ['New Logon[\s\S]*?Account Name(:|=)\s*(-|SYSTEM|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))[\s;]*Account Domain(:|=)', 'TargetUserName\\?"+:\\?"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"'] |
| added_regex_field | src_host |  | ['Workstation Name(:|=)\s*((?-i)\\+[rnt])*(-|[A-Fa-f:\d.]+|({src_host_windows}({src_host}[\w\-\.]+)))[\s;]*((?-i)\\+[rnt])*Source Network Address(:|=)', 'WorkstationName\\?"+:\\?"+(?:-|({src_host_windows}({src_host}[\w\-\.]+)))\\?"'] |
| removed_attribute | DupFields |  | N/A |
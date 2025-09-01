# Code Changes for unix-unix-mix-user-switch-success-sudo (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['agent_id', 'cluster_name', 'current_working_dir', 'dest_host', 'dest_ip', 'dest_user', 'domain', 'email_address', 'event_code', 'event_name', 'group_info', 'group_name', 'host', 'host_ip', 'pci_dss', 'process_command_line', 'process_name', 'process_relative_dir', 'process_relative_path', 'severity', 'time', 'user', 'wazuh_manager'] |
| removed_regex_field | process_dir |  | [] |
| edit_regex_field | process_name |  | ['\WCOMMAND\\?=({process_relative_path}({process_relative_dir}[^\s]+[\\\/]+)?({process_name}[^;\\\/\s]+))\s(?:|;|$)'] |
| removed_regex_field | process_path |  | [] |
| added_regex_field | current_working_dir |  | ['\WPWD\\?=({current_working_dir}[^\s;]+)'] |
| added_regex_field | process_relative_dir |  | ['\WCOMMAND\\?=({process_relative_path}({process_relative_dir}[^\s]+[\\\/]+)?({process_name}[^;\\\/\s]+))\s(?:|;|$)'] |
| added_regex_field | process_relative_path |  | ['\WCOMMAND\\?=({process_relative_path}({process_relative_dir}[^\s]+[\\\/]+)?({process_name}[^;\\\/\s]+))\s(?:|;|$)'] |
# Code Changes for akamai-guardicore-cef-alert-trigger-success-networklog-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'app', 'category', 'connection_type', 'dest_domain', 'dest_host', 'dest_ip', 'dest_port', 'dest_process_dir', 'dest_process_name', 'dest_process_path', 'dest_user', 'event_name', 'protocol', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | protocol |  | ['proto=({protocol}[^=]+)\s+\w+='] |
| removed_regex_field | web_domain |  | [] |
| added_regex_field | app |  | ['cs16=({app}[^=]+)(?:\s+\w+|$)'] |
| added_regex_field | connection_type |  | ['cs1=({connection_type}[^\s]+)\s+\w+='] |
| added_regex_field | dest_host |  | ['dhost=({dest_host}[\w\-\.]+)'] |
| added_regex_field | dest_process_dir |  | ['cs15=({dest_process_path}({dest_process_dir}(?:\w+:|\/)*(?:[\\\/]+[\w\s\.\-\(\)]+)*[\\\/]+)({dest_process_name}[\w\-.]+)*)'] |
| added_regex_field | dest_process_name |  | ['cs15=({dest_process_path}({dest_process_dir}(?:\w+:|\/)*(?:[\\\/]+[\w\s\.\-\(\)]+)*[\\\/]+)({dest_process_name}[\w\-.]+)*)'] |
| added_regex_field | dest_process_path |  | ['cs15=({dest_process_path}({dest_process_dir}(?:\w+:|\/)*(?:[\\\/]+[\w\s\.\-\(\)]+)*[\\\/]+)({dest_process_name}[\w\-.]+)*)'] |
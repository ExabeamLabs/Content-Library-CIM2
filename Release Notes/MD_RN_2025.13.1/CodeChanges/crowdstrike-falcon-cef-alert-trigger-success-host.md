# Code Changes for crowdstrike-falcon-cef-alert-trigger-success-host (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'falcon_host_link', 'file_dir', 'file_name', 'host', 'process_command_line', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| removed_regex_field | file_path |  | [] |
| added_regex_field | file_dir |  | ['(\s|\|)filePath=({file_dir}.+?)\s+(\w+=|$)'] |
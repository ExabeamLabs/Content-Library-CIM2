# Code Changes for vmware-carbonblackedr-leef-alert-trigger-success-feed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'hash_md5', 'host', 'host_type', 'ioc', 'os', 'parent_process_guid', 'parent_process_name', 'path', 'process_command_line', 'process_dir', 'process_guid', 'process_name', 'process_path', 'sensor_id', 'time', 'user'] |
| edit_regex_field | ioc |  | ['\Wioc_query_string=(|({additional_info}({ioc}[^=]+?)))(\s+\w+=|\s*$)', '\Wioc_value=(|({additional_info}({ioc}[^=]+?)))(\s+\w+=|\s*$)'] |
| added_regex_field | additional_info |  | ['\Wioc_query_string=(|({additional_info}({ioc}[^=]+?)))(\s+\w+=|\s*$)', '\Wioc_value=(|({additional_info}({ioc}[^=]+?)))(\s+\w+=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |
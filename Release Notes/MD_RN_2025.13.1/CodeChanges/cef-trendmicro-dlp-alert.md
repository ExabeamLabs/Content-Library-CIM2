# Code Changes for cef-trendmicro-dlp-alert (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'file_dir', 'file_name', 'first_name', 'host', 'last_name', 'policy_guid', 'result', 'src_host', 'src_ip', 'src_port', 'target', 'time', 'user'] |
| removed_regex_field | file_path |  | [] |
| added_regex_field | file_dir |  | ['\WfilePath=({file_dir}.+?)\s+(\w+=|$)'] |
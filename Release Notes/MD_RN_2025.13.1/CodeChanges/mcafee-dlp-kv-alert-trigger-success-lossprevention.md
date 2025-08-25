# Code Changes for mcafee-dlp-kv-alert-trigger-success-lossprevention (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'file_dir', 'file_ext', 'file_name', 'file_path', 'process_dir', 'process_name', 'process_path', 'signature_id', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | file_name |  | ['\WDLP_FileName="({file_path}({file_dir}[^<>]*?[\\\/<>]+)?({file_name}[^\\\/<>]+?(\.({file_ext}\w+))?))"'] |
| added_regex_field | file_dir |  | ['\WDLP_FileName="({file_path}({file_dir}[^<>]*?[\\\/<>]+)?({file_name}[^\\\/<>]+?(\.({file_ext}\w+))?))"'] |
| added_regex_field | file_ext |  | ['\WDLP_FileName="({file_path}({file_dir}[^<>]*?[\\\/<>]+)?({file_name}[^\\\/<>]+?(\.({file_ext}\w+))?))"'] |
| added_regex_field | file_path |  | ['\WDLP_FileName="({file_path}({file_dir}[^<>]*?[\\\/<>]+)?({file_name}[^\\\/<>]+?(\.({file_ext}\w+))?))"'] |
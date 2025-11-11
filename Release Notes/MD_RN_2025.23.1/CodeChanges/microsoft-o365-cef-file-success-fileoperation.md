# Code Changes for microsoft-o365-cef-file-success-fileoperation (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'app', 'domain', 'event_code', 'file_dir', 'file_type', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | access |  | ['\sact=({event_code}({access}.+?))\s+\w+='] |
| added_regex_field | event_code |  | ['\sact=({event_code}({access}.+?))\s+\w+='] |
| removed_attribute | DupFields |  | N/A |
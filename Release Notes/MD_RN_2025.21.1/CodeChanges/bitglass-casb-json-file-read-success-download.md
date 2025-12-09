# Code Changes for bitglass-casb-json-file-read-success-download (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['email_address', 'email_domain', 'file_ext', 'file_name', 'full_name', 'src_file_name', 'src_ip', 'src_port', 'user'] |
| edit_regex_field | file_ext |  | ['exa_json_path=$.filename,exa_regex=\s*"({file_name}({src_file_name}[^"]+?(\.({file_ext}[^."]+))?))",'] |
| edit_regex_field | src_file_name |  | ['exa_json_path=$.filename,exa_regex=\s*"({file_name}({src_file_name}[^"]+?(\.({file_ext}[^."]+))?))",'] |
| added_regex_field | file_name |  | ['exa_json_path=$.filename,exa_regex=\s*"({file_name}({src_file_name}[^"]+?(\.({file_ext}[^."]+))?))",'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for symantec-atp-json-alert-trigger-success-datasourceurlreferer (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_port', 'domain', 'file_dir', 'file_name', 'host', 'malware_url', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| removed_regex_field | file_path |  | [] |
| added_regex_field | file_dir |  | ['"folder":"({file_dir}[^"]+)"'] |
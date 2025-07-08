# Code Changes for microsoft-evapplocker-xml-alert-trigger-success-policyname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'domain', 'event_code', 'hash_md5', 'host', 'malware_url', 'run_level', 'time', 'user', 'user_sid'] | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'domain', 'event_code', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host', 'malware_url', 'process_dir', 'process_name', 'process_path', 'run_level', 'time', 'user', 'user_sid'] |
| edit_regex_field | hash_md5 | ['<FileHash>({hash_md5}[^"<]+)'] | ['<FileHash>(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))'] |
| added_regex_field | hash_sha1 | [] | ['<FileHash>(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))'] |
| added_regex_field | hash_sha256 | [] | ['<FileHash>(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))'] |
| added_regex_field | process_dir | [] | ['<FilePath>({process_path}({process_dir}[^<]*[\\\/]+)?({process_name}[^<]+?))<'] |
| added_regex_field | process_name | [] | ['<FilePath>({process_path}({process_dir}[^<]*[\\\/]+)?({process_name}[^<]+?))<'] |
| added_regex_field | process_path | [] | ['<FilePath>({process_path}({process_dir}[^<]*[\\\/]+)?({process_name}[^<]+?))<'] |
| removed_attribute | DupFields | ['malware_url->process_name'] | N/A |
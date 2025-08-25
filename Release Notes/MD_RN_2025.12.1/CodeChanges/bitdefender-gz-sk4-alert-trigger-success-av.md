# Code Changes for bitdefender-gz-sk4-alert-trigger-success-av (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['alert_id', 'alert_name', 'alert_severity', 'alert_type', 'category', 'count', 'domain', 'email_address', 'hash_md5', 'host', 'last_blocked_time', 'malware_file_name', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'protocol', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] | ['alert_id', 'alert_name', 'alert_severity', 'alert_type', 'category', 'count', 'domain', 'email_address', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host', 'last_blocked_time', 'malware_file_name', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'protocol', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | hash_md5 | ['"hash":"({hash_md5}[^"]+)'] | ['"hash":"(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))"'] |
| added_regex_field | hash_sha1 | [] | ['"hash":"(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))"'] |
| added_regex_field | hash_sha256 | [] | ['"hash":"(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))"'] |
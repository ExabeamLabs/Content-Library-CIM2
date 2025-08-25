# Code Changes for vmware-carbonblackappctrl-kv-alert-trigger-success-execution (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['additional_info', 'alert_name', 'alert_severity', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'file_name', 'file_path', 'hash_md5', 'host', 'process_dir', 'process_name', 'process_path', 'time', 'user'] | ['additional_info', 'alert_name', 'alert_severity', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'file_name', 'file_path', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host', 'process_dir', 'process_name', 'process_path', 'time', 'user'] |
| edit_regex_field | hash_md5 | ['\sfile_hash="({hash_md5}[^"]+)"', '\sfile_hash="({hash_md5}[^"]+)"'] | ['\sfile_hash="(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))"'] |
| added_regex_field | hash_sha1 | [] | ['\sfile_hash="(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))"'] |
| added_regex_field | hash_sha256 | [] | ['\sfile_hash="(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))"'] |
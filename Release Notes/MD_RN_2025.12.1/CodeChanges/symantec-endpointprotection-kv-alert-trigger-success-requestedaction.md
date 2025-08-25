# Code Changes for symantec-endpointprotection-kv-alert-trigger-success-requestedaction (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'bytes', 'dest_host', 'dest_ip', 'dest_port', 'file_hash', 'hash_type', 'host', 'malware_url', 'process_name', 'src_host', 'src_ip', 'src_port', 'time', 'user'] | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'bytes', 'dest_host', 'dest_ip', 'dest_port', 'file_hash', 'hash_md5', 'hash_sha1', 'hash_sha256', 'hash_type', 'host', 'malware_url', 'process_name', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | file_hash | ['Application hash:\s*(|({file_hash}[^,]+)),'] | ['Application hash:\s*(|({file_hash}(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32})))),'] |
| added_regex_field | hash_md5 | [] | ['Application hash:\s*(|({file_hash}(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32})))),'] |
| added_regex_field | hash_sha1 | [] | ['Application hash:\s*(|({file_hash}(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32})))),'] |
| added_regex_field | hash_sha256 | [] | ['Application hash:\s*(|({file_hash}(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32})))),'] |
| removed_attribute | DupFields | ['file_hash->hash_md5'] | N/A |
# Code Changes for symantec-endpointprotection-kv-alert-trigger-success-detecte (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['action', 'additional_info', 'alert_name', 'alert_type', 'event_name', 'hash_md5', 'host', 'process_dir', 'process_name', 'process_path', 'src_ip', 'src_port', 'time', 'user'] | ['action', 'additional_info', 'alert_name', 'alert_type', 'event_name', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host', 'process_dir', 'process_name', 'process_path', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | hash_md5 | ['Hachage d’application\xa0:\s({hash_md5}[^,]+)'] | ['Hachage d’application\xa0:\s(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))'] |
| added_regex_field | hash_sha1 | [] | ['Hachage d’application\xa0:\s(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))'] |
| added_regex_field | hash_sha256 | [] | ['Hachage d’application\xa0:\s(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))'] |
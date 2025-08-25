# Code Changes for eset-es-leef-http-session-fail-eset (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['action', 'additional_info', 'category', 'dest_ip', 'dest_port', 'direction', 'domain', 'event_name', 'hash_sha256', 'host', 'operation', 'process_dir', 'process_name', 'process_path', 'protocol', 'result', 'src_ip', 'src_port', 'time', 'url', 'user'] | ['action', 'additional_info', 'category', 'dest_ip', 'dest_port', 'direction', 'domain', 'event_name', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host', 'operation', 'process_dir', 'process_name', 'process_path', 'protocol', 'result', 'src_ip', 'src_port', 'time', 'url', 'user'] |
| edit_regex_field | hash_sha256 | ['hash=({hash_sha256}[^\s]+)'] | ['hash=(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))'] |
| added_regex_field | hash_md5 | [] | ['hash=(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))'] |
| added_regex_field | hash_sha1 | [] | ['hash=(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))'] |
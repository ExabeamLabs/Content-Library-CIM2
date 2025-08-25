# Code Changes for trendmicro-ds-cef-network-traffic-fail-idsdeny (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['additional_info', 'bytes_in', 'bytes_out', 'dest_host', 'dest_ip', 'dest_mac', 'dest_port', 'file_dir', 'file_ext', 'file_hash', 'file_name', 'file_path', 'hash_md5', 'hash_sha1', 'host', 'method', 'operation', 'protocol', 'rule', 'src_ip', 'src_mac', 'src_port', 'suid', 'user'] | ['additional_info', 'bytes_in', 'bytes_out', 'dest_host', 'dest_ip', 'dest_mac', 'dest_port', 'file_dir', 'file_ext', 'file_hash', 'file_name', 'file_path', 'host', 'method', 'operation', 'protocol', 'rule', 'src_ip', 'src_mac', 'src_port', 'suid', 'user'] |
| removed_regex_field | hash_md5 | ['cs3=({hash_md5}[^\s]+)'] | [] |
| removed_regex_field | hash_sha1 | ['cs2=({hash_sha1}[^\s]+)'] | [] |
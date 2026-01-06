# Code Changes for vectra-cs-kv-ssh-traffic-success-metadatassh (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['cipher_algorithm', 'client_version', 'compression_algorithm', 'dest_host', 'dest_ip', 'dest_port', 'server_version', 'src_host', 'src_ip', 'src_port', 'time'] |
| removed_regex_field | compression_algotithm |  | [] |
| added_regex_field | compression_algorithm |  | ['compression_alg="+(none|({compression_algorithm}[^"]+))"+'] |
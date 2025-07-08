# Code Changes for cisco-fp-json-alert-trigger-success-502 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['dest_ip', 'dest_port', 'src_ip', 'src_port', 'time', 'user'] | ['dest_ip', 'dest_port', 'hash_md5', 'hash_sha1', 'hash_sha256', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | hash_md5 | [] | ['exa_json_path=$.shaHash,exa_regex=^(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))$'] |
| added_regex_field | hash_sha1 | [] | ['exa_json_path=$.shaHash,exa_regex=^(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))$'] |
| added_regex_field | hash_sha256 | [] | ['exa_json_path=$.shaHash,exa_regex=^(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))$'] |
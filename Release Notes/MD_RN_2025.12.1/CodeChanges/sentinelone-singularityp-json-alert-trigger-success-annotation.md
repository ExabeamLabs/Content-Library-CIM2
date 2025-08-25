# Code Changes for sentinelone-singularityp-json-alert-trigger-success-annotation (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | hash_md5 | ['exa_regex="fileContentHash":\s*"(({hash_md5}\w{32})|({hash_sha1}\w{40})|({hash_sha256}\w{64}))"'] | ['exa_regex="fileContentHash":\s*"(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))"'] |
| edit_regex_field | hash_sha1 | ['exa_regex="fileContentHash":\s*"(({hash_md5}\w{32})|({hash_sha1}\w{40})|({hash_sha256}\w{64}))"'] | ['exa_regex="fileContentHash":\s*"(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))"'] |
| edit_regex_field | hash_sha256 | ['exa_regex="fileContentHash":\s*"(({hash_md5}\w{32})|({hash_sha1}\w{40})|({hash_sha256}\w{64}))"'] | ['exa_regex="fileContentHash":\s*"(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))"'] |
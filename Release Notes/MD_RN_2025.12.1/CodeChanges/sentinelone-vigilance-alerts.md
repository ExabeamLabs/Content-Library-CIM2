# Code Changes for sentinelone-vigilance-alerts (ParserTemplate)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | hash_md5 | ['fileHash=(({hash_md5}\w{32})|({hash_sha1}\w{40})|({hash_sha256}\w{64}))\s\w+='] | ['fileHash=(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))\s\w+='] |
| edit_regex_field | hash_sha1 | ['fileHash=(({hash_md5}\w{32})|({hash_sha1}\w{40})|({hash_sha256}\w{64}))\s\w+='] | ['fileHash=(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))\s\w+='] |
| edit_regex_field | hash_sha256 | ['fileHash=(({hash_md5}\w{32})|({hash_sha1}\w{40})|({hash_sha256}\w{64}))\s\w+='] | ['fileHash=(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))\s\w+='] |
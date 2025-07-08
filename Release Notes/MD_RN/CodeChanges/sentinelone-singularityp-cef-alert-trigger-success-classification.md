# Code Changes for sentinelone-singularityp-cef-alert-trigger-success-classification (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | hash_md5 | ['"fileContentHash":"(({hash_md5}\w{32})|({hash_sha1}\w{40})|({hash_sha256}\w{64}))"'] | ['"fileContentHash":"(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))"'] |
| edit_regex_field | hash_sha1 | ['"fileContentHash":"(({hash_md5}\w{32})|({hash_sha1}\w{40})|({hash_sha256}\w{64}))"', '"sha1":"({hash_sha1}[^",]+)'] | ['"fileContentHash":"(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))"', '"sha1":"({hash_sha1}[^",]+)'] |
| edit_regex_field | hash_sha256 | ['"fileContentHash":"(({hash_md5}\w{32})|({hash_sha1}\w{40})|({hash_sha256}\w{64}))"'] | ['"fileContentHash":"(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))"'] |
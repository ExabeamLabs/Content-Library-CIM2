# Code Changes for sentinelone-singularityp-cef-process-create-success-visibility (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | hash_md5 | ['\smd5:\s*[\\\/]?"+({hash_md5}[^"\\]+)'] | ['\smd5:\s*[\\\/]?"+({hash_md5}\w+)'] |
| edit_regex_field | hash_sha1 | ['sha1:\s*"*({hash_sha1}[^"]+)"'] | ['sha1:\s*[\\\/]?"+({hash_sha1}\w+)"'] |
| edit_regex_field | hash_sha256 | ['\ssha256:\s*[\\\/]?"+({hash_sha256}[^"\\]+)'] | ['\ssha256:\s*[\\\/]?"+({hash_sha256}\w+)'] |
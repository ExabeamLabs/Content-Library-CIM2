# Code Changes for sentinelone-s-cef-http-session-success-visibility-1 (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | hash_md5 | ['\smd5:\s*[\\\/]?"+({hash_md5}[^"\\]+)'] | ['\smd5:\s*[\\\/]?"+({hash_md5}\w+)'] |
| edit_regex_field | hash_sha1 | ['sha1:\s*"*({hash_sha1}[^"]+)"'] | ['sha1:\s*[\\\/]?"+({hash_sha1}\w+)"'] |
| edit_regex_field | hash_sha256 | ['\ssha256:\s*[\\\/]?"+({hash_sha256}[^"\\]+)'] | ['\ssha256:\s*[\\\/]?"+({hash_sha256}\w+)'] |
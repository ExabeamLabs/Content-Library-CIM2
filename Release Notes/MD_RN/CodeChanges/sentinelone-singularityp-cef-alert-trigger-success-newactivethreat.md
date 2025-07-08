# Code Changes for sentinelone-singularityp-cef-alert-trigger-success-newactivethreat (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | hash_md5 | ['\WfileHash=(N/A|(({hash_md5}\w{32})|({hash_sha1}\w{40})|({hash_sha256}\w{64})))((\||\s+)\w+=|\s*$)'] | ['\WfileHash=(N/A|(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32})))((\||\s+)\w+=|\s*$)'] |
| edit_regex_field | hash_sha1 | ['\WfileHash=(N/A|(({hash_md5}\w{32})|({hash_sha1}\w{40})|({hash_sha256}\w{64})))((\||\s+)\w+=|\s*$)'] | ['\WfileHash=(N/A|(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32})))((\||\s+)\w+=|\s*$)'] |
| edit_regex_field | hash_sha256 | ['\WfileHash=(N/A|(({hash_md5}\w{32})|({hash_sha1}\w{40})|({hash_sha256}\w{64})))((\||\s+)\w+=|\s*$)'] | ['\WfileHash=(N/A|(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32})))((\||\s+)\w+=|\s*$)'] |
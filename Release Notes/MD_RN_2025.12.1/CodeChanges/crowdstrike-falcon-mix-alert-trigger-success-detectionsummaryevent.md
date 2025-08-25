# Code Changes for crowdstrike-falcon-mix-alert-trigger-success-detectionsummaryevent (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | hash_md5 | ['"MD5String"+:"+({hash_md5}[^"]+)"'] | ['"MD5String"+:"+({hash_md5}[^",]+)"'] |
| edit_regex_field | hash_sha256 | ['"SHA256String":"({hash_sha256}[^"]+)'] | ['"SHA256String":"({hash_sha256}[^",]+)'] |
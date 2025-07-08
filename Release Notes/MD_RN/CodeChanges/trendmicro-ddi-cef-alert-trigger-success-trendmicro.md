# Code Changes for trendmicro-ddi-cef-alert-trigger-success-trendmicro (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'dest_ip', 'dest_port', 'hash_md5', 'host', 'malware_url', 'result', 'src_host', 'src_ip', 'src_mac', 'src_port', 'time'] | ['alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'dest_ip', 'dest_port', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host', 'malware_url', 'result', 'src_host', 'src_ip', 'src_mac', 'src_port', 'time'] |
| edit_regex_field | hash_md5 | ['\WcompressedFileHash=({hash_md5}.+?)(\s+\w+=|\s*$)'] | ['\WcompressedFileHash=(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))(\s+\w+=|\s*$)'] |
| added_regex_field | hash_sha1 | [] | ['\WcompressedFileHash=(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))(\s+\w+=|\s*$)'] |
| added_regex_field | hash_sha256 | [] | ['\WcompressedFileHash=(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))(\s+\w+=|\s*$)'] |
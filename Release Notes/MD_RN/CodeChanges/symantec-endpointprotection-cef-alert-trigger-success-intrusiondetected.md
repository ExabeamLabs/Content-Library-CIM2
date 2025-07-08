# Code Changes for symantec-endpointprotection-cef-alert-trigger-success-intrusiondetected (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_ip', 'dest_port', 'hash_md5', 'host', 'malware_file_name', 'malware_url', 'process_name', 'result', 'scan_type', 'secondary_action', 'src_host', 'src_ip', 'src_port', 'time', 'user'] | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_ip', 'dest_port', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host', 'malware_file_name', 'malware_url', 'process_name', 'result', 'scan_type', 'secondary_action', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | hash_md5 | ['\sfileHash=({hash_md5}[^\s]+)'] | ['\sfileHash=(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))\s+'] |
| added_regex_field | hash_sha1 | [] | ['\sfileHash=(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))\s+'] |
| added_regex_field | hash_sha256 | [] | ['\sfileHash=(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))\s+'] |
# Code Changes for cynet-cynetedr-cef-alert-trigger-success-endpointalert (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['additional_info', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'command', 'dest_host', 'domain', 'file_name', 'file_path', 'hash_md5', 'os', 'risk_level', 'src_ip', 'src_port', 'time', 'user'] | ['additional_info', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'command', 'dest_host', 'domain', 'file_name', 'file_path', 'hash_md5', 'hash_sha1', 'hash_sha256', 'os', 'risk_level', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | hash_md5 | ['\WfileHash=({hash_md5}[^\s]+)'] | ['\WfileHash=(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))\s*(\w+=|\$)'] |
| added_regex_field | hash_sha1 | [] | ['\WfileHash=(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))\s*(\w+=|\$)'] |
| added_regex_field | hash_sha256 | [] | ['\WfileHash=(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))\s*(\w+=|\$)'] |
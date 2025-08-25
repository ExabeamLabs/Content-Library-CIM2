# Code Changes for eset-es-leef-alert-trigger-success-threatevent (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['action', 'alert_name', 'alert_severity', 'alert_type', 'circumstances', 'domain', 'engine_version', 'firstseen', 'hash_sha256', 'host', 'malware_url', 'object_type', 'result_code', 'src_ip', 'src_port', 'threat_category', 'threat_handled', 'time', 'user'] | ['action', 'alert_name', 'alert_severity', 'alert_type', 'circumstances', 'domain', 'engine_version', 'firstseen', 'hash_sha256', 'host', 'malware_url', 'object_type', 'process_dir', 'process_name', 'process_path', 'result_code', 'src_ip', 'src_port', 'threat_category', 'threat_handled', 'time', 'user'] |
| added_regex_field | process_dir | [] | ['objectUri=({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?))\s*(\w+=|$)'] |
| added_regex_field | process_name | [] | ['objectUri=({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?))\s*(\w+=|$)'] |
| added_regex_field | process_path | [] | ['objectUri=({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?))\s*(\w+=|$)'] |
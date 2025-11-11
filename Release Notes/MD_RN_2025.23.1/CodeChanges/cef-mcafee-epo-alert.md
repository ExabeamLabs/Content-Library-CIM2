# Code Changes for cef-mcafee-epo-alert (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_severity', 'alert_type', 'domain', 'file_name', 'host', 'malware_file_name', 'malware_url', 'result', 'src_host', 'src_ip', 'src_port', 'threat_category', 'time', 'user'] |
| edit_regex_field | malware_file_name |  | ['\sfname=({malware_url}[^=]+?\\+({file_name}({malware_file_name}[^\\=]+?)))\s+\w+='] |
| edit_regex_field | malware_url |  | ['\sfname=({malware_url}.+?)\s+(\w+=)', '\sfname=({malware_url}[^=]+?\\+({file_name}({malware_file_name}[^\\=]+?)))\s+\w+='] |
| added_regex_field | file_name |  | ['\sfname=({malware_url}[^=]+?\\+({file_name}({malware_file_name}[^\\=]+?)))\s+\w+='] |
| removed_attribute | DupFields |  | N/A |
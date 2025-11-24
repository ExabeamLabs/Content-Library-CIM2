# Code Changes for blackberry-protect-sk4-alert-trigger-success-cyclaneprotect (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_source', 'alert_subject', 'alert_type', 'bytes', 'category', 'device_name', 'file_hash', 'file_name', 'hash_md5', 'hash_sha256_at', 'malware_url', 'name_at', 'process_dir', 'process_name', 'process_path', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | alert_type |  | ['Security Alert Detected by.*?Category \[({alert_name}({alert_type}[^\]\[,]+?))\]', '\Wcat=(|({alert_name}({alert_type}.+?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | device_name |  | ['\WdestinationServiceName=(|({alert_source}({device_name}.+?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | file_hash |  | ['"sha256":"({hash_sha256_at}({file_hash}[^"]+))"'] |
| edit_regex_field | file_name |  | ['"name":"({name_at}({file_name}[^"]+))"', '\Wproto=(|({name_at}({file_name}.+?)))(\s+\w+=|\s*$)'] |
| added_regex_field | alert_name |  | ['Security Alert Detected by.*?Category \[({alert_name}({alert_type}[^\]\[,]+?))\]', '\Wcat=(|({alert_name}({alert_type}.+?)))(\s+\w+=|\s*$)'] |
| added_regex_field | alert_source |  | ['\WdestinationServiceName=(|({alert_source}({device_name}.+?)))(\s+\w+=|\s*$)'] |
| added_regex_field | hash_sha256_at |  | ['"sha256":"({hash_sha256_at}({file_hash}[^"]+))"'] |
| added_regex_field | name_at |  | ['"name":"({name_at}({file_name}[^"]+))"', '\Wproto=(|({name_at}({file_name}.+?)))(\s+\w+=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |
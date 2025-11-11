# Code Changes for pan-ngfw-json-alert-trigger-success-threat (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'dest_ip', 'dest_port', 'dest_translated_ip', 'domain', 'email_address', 'host', 'malware_url', 'src_ip', 'src_port', 'src_translated_ip', 'threat_category', 'url', 'user'] |
| edit_regex_field | malware_url |  | ['exa_json_path=$..URL,exa_regex=({url}({malware_url}[^\/"]+))'] |
| added_regex_field | url |  | ['exa_json_path=$..URL,exa_regex=({url}({malware_url}[^\/"]+))'] |
| removed_attribute | DupFields |  | N/A |
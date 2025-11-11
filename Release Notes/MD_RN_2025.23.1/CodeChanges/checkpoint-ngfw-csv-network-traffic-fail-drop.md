# Code Changes for checkpoint-ngfw-csv-network-traffic-fail-drop (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'dest_ip', 'dest_port', 'dest_translated_ip', 'dest_translated_port', 'direction', 'email_subject', 'host', 'protocol', 'rule', 'src_host', 'src_ip', 'src_port', 'src_translated_ip', 'src_translated_port', 'time', 'users'] |
| added_regex_field | email_subject |  | ['\WAction=(-|({email_subject}.+?))(\s+[\w-]+=|"+\s*$|\|)'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for cisco-fp-kv-alert-trigger-success-correlationevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_type', 'category', 'dest_country', 'dest_ip', 'dest_port', 'host', 'policy_name', 'protocol', 'src_country', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | host |  | ['({host}[\w\-.]+) SFIMS:\s*Correlation Event:\s*({alert_name}({policy_name}.+?)) (correlation policy|on Discovered host|on Security Intelligence) at ({time}\w+ \w+ \d\d \d\d:\d\d:\d\d \d\d\d\d \w+?)\s*(Connection Type|:)', '\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD'] |
| edit_regex_field | policy_name |  | ['({host}[\w\-.]+) SFIMS:\s*Correlation Event:\s*({alert_name}({policy_name}.+?)) (correlation policy|on Discovered host|on Security Intelligence) at ({time}\w+ \w+ \d\d \d\d:\d\d:\d\d \d\d\d\d \w+?)\s*(Connection Type|:)'] |
| edit_regex_field | time |  | ['({host}[\w\-.]+) SFIMS:\s*Correlation Event:\s*({alert_name}({policy_name}.+?)) (correlation policy|on Discovered host|on Security Intelligence) at ({time}\w+ \w+ \d\d \d\d:\d\d:\d\d \d\d\d\d \w+?)\s*(Connection Type|:)'] |
| added_regex_field | alert_name |  | ['({host}[\w\-.]+) SFIMS:\s*Correlation Event:\s*({alert_name}({policy_name}.+?)) (correlation policy|on Discovered host|on Security Intelligence) at ({time}\w+ \w+ \d\d \d\d:\d\d:\d\d \d\d\d\d \w+?)\s*(Connection Type|:)'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for pan-ngfw-csv-network-traffic-success-allow (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | action | ['TRAFFIC,([^,]*,){26}({action}[^,]+?)\s*,'] | [',TRAFFIC,([^,]*,){26}({action}[^,]+?)\s*,'] |
| edit_regex_field | bytes | ['TRAFFIC,([^,]*,){27}({bytes}\d+)'] | [',TRAFFIC,([^,]*,){27}({bytes}\d+)'] |
| edit_regex_field | bytes_in | ['TRAFFIC,([^,]*,){29}({bytes_in}\d+)'] | [',TRAFFIC,([^,]*,){29}({bytes_in}\d+)'] |
| edit_regex_field | bytes_out | ['TRAFFIC,([^,]*,){28}({bytes_out}\d+)'] | [',TRAFFIC,([^,]*,){28}({bytes_out}\d+)'] |
| edit_regex_field | category | ['TRAFFIC,([^,]*,){33}(any|unknown|({category}[^,]+?)\s*,)'] | [',TRAFFIC,([^,]*,){33}(any|unknown|({category}[^,]+?)\s*,)'] |
| edit_regex_field | dest_country | ['TRAFFIC,([^,]*,){38}({dest_country}[^\.:]*?)\s*,'] | [',TRAFFIC,([^,]*,){38}({dest_country}[^\.:]*?)\s*,'] |
| edit_regex_field | dest_domain | ['TRAFFIC,([^,]*,){9}\s*(?:({dest_domain}[^\s,\\]+)\\)?({dest_user}[^\s,]+),'] | [',TRAFFIC,([^,]*,){9}\s*(?:({dest_domain}[^\s,\\]+)\\)?({dest_user}[^\s,]+),'] |
| edit_regex_field | dest_ip | ['TRAFFIC,([^,]*,){4}(0.0.0.0|({dest_ip}(?!::)[a-fA-F\d.:]+))'] | [',TRAFFIC,([^,]*,){4}(0.0.0.0|({dest_ip}(?!::)[a-fA-F\d.:]+))'] |
| edit_regex_field | dest_network_zone | ['TRAFFIC,([^,]*,){13}({dest_network_zone}[^,]+?)\s*,'] | [',TRAFFIC,([^,]*,){13}({dest_network_zone}[^,]+?)\s*,'] |
| edit_regex_field | dest_port | ['TRAFFIC,([^,]*,){21}(0|({dest_port}\d+)),'] | [',TRAFFIC,([^,]*,){21}(0|({dest_port}\d+)),'] |
| edit_regex_field | dest_translated_ip | ['TRAFFIC,([^,]*,){6}(0.0.0.0|({dest_translated_ip}(?!::)[a-fA-F\d.:]+))'] | [',TRAFFIC,([^,]*,){6}(0.0.0.0|({dest_translated_ip}(?!::)[a-fA-F\d.:]+))'] |
| edit_regex_field | dest_translated_port | ['TRAFFIC,([^,]*,){23}(0|({dest_translated_port}\d+)),'] | [',TRAFFIC,([^,]*,){23}(0|({dest_translated_port}\d+)),'] |
| edit_regex_field | dest_user | ['TRAFFIC,([^,]*,){9}\s*(?:({dest_domain}[^\s,\\]+)\\)?({dest_user}[^\s,]+),'] | [',TRAFFIC,([^,]*,){9}\s*(?:({dest_domain}[^\s,\\]+)\\)?({dest_user}[^\s,]+),'] |
| edit_regex_field | email_address | ['TRAFFIC,([^,]*,){8}\s*(({email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({src_domain}[^\s,\\]+)\\)?({src_user}[^\s,]+)),'] | [',TRAFFIC,([^,]*,){8}\s*(({email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({src_domain}[^\s,\\]+)\\)?({src_user}[^\s,]+)),'] |
| edit_regex_field | host | [':\d\d:\d\d(([+-]\d\d:\d\d)|(\.\d+Z))?\s+({host}[\w.-]+)\s', 'TRAFFIC,("[^"]*",|[^,]*,){48}({host}[\w\-\.]+)', '\s({host}[^\s]+)\s+(\[.*?\]\s+)?\d+,([^,]*,){2}TRAFFIC,'] | [',TRAFFIC,("[^"]*",|[^,]*,){48}({host}[\w\-\.]+)', ':\d\d:\d\d(([+-]\d\d:\d\d)|(\.\d+Z))?\s+({host}[\w.-]+)\s', '\s({host}[^\s]+)\s+(\[.*?\]\s+)?\d+,([^,]*,){2}TRAFFIC,'] |
| edit_regex_field | network_app | ['TRAFFIC,([^,]*,){10}(not-applicable|({network_app}[^,]+?))\s*,'] | [',TRAFFIC,([^,]*,){10}(not-applicable|({network_app}[^,]+?))\s*,'] |
| edit_regex_field | protocol | ['TRAFFIC,([^,]*,){25}({protocol}[^,]+?)\s*,'] | [',TRAFFIC,([^,]*,){25}({protocol}[^,]+?)\s*,'] |
| edit_regex_field | rule | ['TRAFFIC,([^,]*,){7}({rule}[^,]+?)\s*,'] | [',TRAFFIC,([^,]*,){7}({rule}[^,]+?)\s*,'] |
| edit_regex_field | session_id | ['TRAFFIC,([^,]*,){18}({session_id}\d+),'] | [',TRAFFIC,([^,]*,){18}({session_id}\d+),'] |
| edit_regex_field | src_country | ['TRAFFIC,([^,]*,){37}({src_country}[^\.:]*?)\s*,'] | [',TRAFFIC,([^,]*,){37}({src_country}[^\.:]*?)\s*,'] |
| edit_regex_field | src_domain | ['TRAFFIC,([^,]*,){8}\s*(({email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({src_domain}[^\s,\\]+)\\)?({src_user}[^\s,]+)),'] | [',TRAFFIC,([^,]*,){8}\s*(({email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({src_domain}[^\s,\\]+)\\)?({src_user}[^\s,]+)),'] |
| edit_regex_field | src_ip | ['TRAFFIC,([^,]*,){3}(0.0.0.0|({src_ip}(?!::)[a-fA-F\d.:]+))'] | [',TRAFFIC,([^,]*,){3}(0.0.0.0|({src_ip}(?!::)[a-fA-F\d.:]+))'] |
| edit_regex_field | src_network_zone | ['TRAFFIC,([^,]*,){12}({src_network_zone}[^,]+?)\s*,'] | [',TRAFFIC,([^,]*,){12}({src_network_zone}[^,]+?)\s*,'] |
| edit_regex_field | src_port | ['TRAFFIC,([^,]*,){20}(0|({src_port}\d+)),'] | [',TRAFFIC,([^,]*,){20}(0|({src_port}\d+)),'] |
| edit_regex_field | src_translated_ip | ['TRAFFIC,([^,]*,){5}(0.0.0.0|({src_translated_ip}(?!::)[a-fA-F\d.:]+))'] | [',TRAFFIC,([^,]*,){5}(0.0.0.0|({src_translated_ip}(?!::)[a-fA-F\d.:]+))'] |
| edit_regex_field | src_translated_port | ['TRAFFIC,([^,]*,){22}(0|({src_translated_port}\d+)),'] | [',TRAFFIC,([^,]*,){22}(0|({src_translated_port}\d+)),'] |
| edit_regex_field | src_user | ['TRAFFIC,([^,]*,){8}\s*(({email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({src_domain}[^\s,\\]+)\\)?({src_user}[^\s,]+)),'] | [',TRAFFIC,([^,]*,){8}\s*(({email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({src_domain}[^\s,\\]+)\\)?({src_user}[^\s,]+)),'] |
| edit_regex_field | subtype | ['TRAFFIC,({subtype}[^,]+),'] | [',TRAFFIC,({subtype}[^,]+),'] |
| edit_regex_field | time | ['((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))', 'TRAFFIC,([^,]*,){2}({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)', 'TRAFFIC,([^,]*,){2}({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+)'] | ['((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))', ',TRAFFIC,([^,]*,){2}({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)', ',TRAFFIC,([^,]*,){2}({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+)'] |
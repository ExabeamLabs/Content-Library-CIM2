# Code Changes for pan-ngfw-csv-alert-trigger-success-file (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_source', 'alert_type', 'app', 'categories', 'category', 'dest_country', 'dest_domain', 'dest_email_address', 'dest_interface', 'dest_ip', 'dest_network_zone', 'dest_port', 'dest_translated_ip', 'dest_translated_port', 'dest_user', 'device_name', 'direction', 'domain', 'email_address', 'event_category', 'file_ext', 'file_name', 'host', 'malware_file_name', 'malware_url', 'network_app', 'protocol', 'result_code', 'rule', 'serial_num', 'session_id', 'severity', 'src_domain', 'src_interface', 'src_ip', 'src_location', 'src_network_zone', 'src_port', 'src_translated_ip', 'src_translated_port', 'src_user', 'threat_category', 'threat_id', 'time', 'url', 'user', 'virtual_station_name', 'web_domain'] |
| edit_regex_field | action |  | [',THREAT,([^,]*,){26}({action}[^,]+?),'] |
| edit_regex_field | alert_id |  | [',THREAT,([^,]*,){28}(|({alert_name}[^\(,]+(\(\w+\))?))\s*\(({alert_id}\d+)?', ',THREAT,file,((""|".*?[^"]"|[^,]*),){31}({alert_id}\d+)(,|$)', ',THREAT,file,([^,]*,){27}(|({additional_info}[^\(,]+(\(\w+\))?))\s*\(({alert_id}\d+)?', ',THREAT,file,([^,]*,){27}(|({alert_name}[^\(,]+(\(\w+\))?))\s*\(({alert_id}\d+)?'] |
| edit_regex_field | alert_name |  | [',THREAT,([^,]*,){28}(|({alert_name}[^\(,]+(\(\w+\))?))\s*\(({alert_id}\d+)?', ',THREAT,({alert_type}({alert_name}[^,]+)),', ',THREAT,file,([^,]*,){27}(|({alert_name}[^\(,]+(\(\w+\))?))\s*\(({alert_id}\d+)?'] |
| edit_regex_field | alert_type |  | [',THREAT,({alert_type}({alert_name}[^,]+)),'] |
| edit_regex_field | app |  | [',THREAT,([^,]*,){10}({alert_source}({network_app}({app}[^,]+))),'] |
| edit_regex_field | dest_domain |  | [',THREAT,([^,]*,){9}\s*(({dest_email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({dest_domain}[^\s,\\]+)\\*)?({dest_user}[^\s,]+)),', ',THREAT,file,([^,]*,){8}(|({dest_domain}[^\\,]+))\\?(|({dest_user}[^\\,]+))(,|$)'] |
| edit_regex_field | dest_email_address |  | [',THREAT,([^,]*,){9}\s*(({dest_email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({dest_domain}[^\s,\\]+)\\*)?({dest_user}[^\s,]+)),'] |
| edit_regex_field | dest_interface |  | [',THREAT,([^,]*,){15}({dest_interface}[^,]+),'] |
| edit_regex_field | dest_ip |  | [',THREAT,([^,]*,){4}({dest_ip}(?!::)[a-fA-F\d.:]+)'] |
| edit_regex_field | dest_network_zone |  | [',THREAT,([^,]*,){13}({dest_network_zone}[^,]+?)\s*,'] |
| edit_regex_field | dest_port |  | [',THREAT,([^,]*,){21}({dest_port}\d+),'] |
| edit_regex_field | dest_translated_ip |  | [',THREAT,([^,]*,){6}({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))'] |
| edit_regex_field | dest_translated_port |  | [',THREAT,([^,]*,){23}({dest_translated_port}\d+)'] |
| edit_regex_field | dest_user |  | [',THREAT,([^,]*,){9}\s*(({dest_email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({dest_domain}[^\s,\\]+)\\*)?({dest_user}[^\s,]+)),', ',THREAT,file,([^,]*,){8}(|({dest_domain}[^\\,]+))\\?(|({dest_user}[^\\,]+))(,|$)'] |
| edit_regex_field | email_address |  | [',THREAT,([^,]*,){8}\s*(({email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({src_domain}[^\s,\\]+)\\*)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))),'] |
| edit_regex_field | file_name |  | [',THREAT,([^,]*,){27}([\\"]*(({url}({malware_url}[^<>".,]+(?:\.[^<>\/\s,]+)?\/[^<>]*?))|({file_name}({malware_file_name}[^<>,]+?)|[^,]*?)[\\\/]*"+,))', ',THREAT,file,((""|".*?[^"]"|[^,]*),){26}"?(?:|({file_name}[^.",]+?(\.({file_ext}[^,."?_]{1,5}))?))\s*("|,)', ',THREAT,file,((""|"[^"]+?"|[^,]*),){26}("(?:|({file_name}[^."]+?(\.({file_ext}[^,."?_]{1,5}))?))\s*",|("")?,)', ',THREAT,file,([^,]*,){26}"*(|({file_name}[^\n]+?(\.({file_ext}[^",\-\.\_\/]+?))?))\s*\/?"*\/?,', ',THREAT,file,([^,]*,){26}"?(?:|({file_name}[^.",]+?(\.({file_ext}[^,."?_]{1,5}))?))\s*("|,)'] |
| edit_regex_field | malware_file_name |  | [',THREAT,([^,]*,){27}([\\"]*(({url}({malware_url}[^<>".,]+(?:\.[^<>\/\s,]+)?\/[^<>]*?))|({file_name}({malware_file_name}[^<>,]+?)|[^,]*?)[\\\/]*"+,))'] |
| edit_regex_field | malware_url |  | [',THREAT,([^,]*,){27}([\\"]*(({url}({malware_url}[^<>".,]+(?:\.[^<>\/\s,]+)?\/[^<>]*?))|({file_name}({malware_file_name}[^<>,]+?)|[^,]*?)[\\\/]*"+,))'] |
| edit_regex_field | network_app |  | [',THREAT,([^,]*,){10}({alert_source}({network_app}({app}[^,]+))),'] |
| edit_regex_field | protocol |  | [',THREAT,([^,]*,){25}({protocol}[^,]+?),'] |
| edit_regex_field | result_code |  | [',THREAT,([^,]*,){24}({result_code}[^,]+),'] |
| edit_regex_field | session_id |  | [',THREAT,([^,]*,){18}({session_id}\d+),'] |
| edit_regex_field | src_domain |  | [',THREAT,([^,]*,){8}\s*(({email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({src_domain}[^\s,\\]+)\\*)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))),'] |
| edit_regex_field | src_interface |  | [',THREAT,([^,]*,){14}({src_interface}[^,]+),'] |
| edit_regex_field | src_ip |  | [',THREAT,([^,]*,){3}({src_ip}(?!::)[a-fA-F\d.:]+)'] |
| edit_regex_field | src_network_zone |  | [',THREAT,([^,]*,){12}({src_network_zone}[^,]+?)\s*,'] |
| edit_regex_field | src_port |  | [',THREAT,([^,]*,){20}({src_port}\d+),'] |
| edit_regex_field | src_translated_ip |  | [',THREAT,([^,]*,){5}({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))'] |
| edit_regex_field | src_translated_port |  | [',THREAT,([^,]*,){22}({src_translated_port}\d+)'] |
| edit_regex_field | src_user |  | [',THREAT,([^,]*,){8}\s*(({email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({src_domain}[^\s,\\]+)\\*)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))),'] |
| edit_regex_field | threat_category |  | [',THREAT,([^,]*,){65}({threat_category}[^,]+),'] |
| edit_regex_field | time |  | [',((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+)),', ',THREAT,([^,]*,){2}({time}[^,]+),'] |
| edit_regex_field | url |  | [',THREAT,([^,]*,){27}([\\"]*(({url}({malware_url}[^<>".,]+(?:\.[^<>\/\s,]+)?\/[^<>]*?))|({file_name}({malware_file_name}[^<>,]+?)|[^,]*?)[\\\/]*"+,))'] |
| edit_regex_field | user |  | [',THREAT,([^,]*,){8}\s*(({email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({src_domain}[^\s,\\]+)\\*)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))),', ',THREAT,file,([^,]*,){7}(?:({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\.,]+\.[^,]+)|(?:|({=domain}[^\\,]+))\\?(?:|({=user}[^\\,]+)))(,|$)'] |
| edit_regex_field | virtual_station_name |  | [',THREAT,([^,]*,){11}({virtual_station_name}[^,]+),'] |
| edit_regex_field | web_domain |  | [',THREAT,([^,]*,){27}\\?("+)?.*?({web_domain}[^\/\.\s]+(?i)(\.(com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ai|ms|mx))+)[\\\/\s:"]'] |
| added_regex_field | additional_info |  | [',THREAT,file,([^,]*,){27}(|({additional_info}[^\(,]+(\(\w+\))?))\s*\(({alert_id}\d+)?'] |
| added_regex_field | alert_source |  | [',THREAT,([^,]*,){10}({alert_source}({network_app}({app}[^,]+))),'] |
| removed_attribute | DupFields |  | N/A |
| edit_attribute | SOAR |  | ConfigTree([('IncidentType', 'malware'), ('NameTemplate', 'Palo Alto Alert ${alert_name} found'), ('ProjectName', 'SOC'), ('EntityFields', [ConfigTree([('EntityType', 'device'), ('Name', 'src_address'), ('Fields', ['src_ip->ip_address'])]), ConfigTree([('EntityType', 'device'), ('Name', 'dest_address'), ('Fields', ['dest_ip->ip_address'])]), ConfigTree([('EntityType', 'user'), ('Name', 'windows_id'), ('Fields', ['user->windows_id'])])])]) |
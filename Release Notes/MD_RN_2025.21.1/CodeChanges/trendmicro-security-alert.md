# Code Changes for trendmicro-security-alert (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_severity', 'alert_type', 'dest_host', 'dest_ip', 'host', 'malware_url', 'src_host', 'src_ip', 'threat_category', 'time'] |
| edit_regex_field | host |  | ['\Wdvchost=({src_host}({host}.+?))\s*(\w+=|$)', '\d\d:\d\d:\d\d\S+\s({src_host}({host}[\w\-\.]+))'] |
| edit_regex_field | threat_category |  | ['\Wcat=({alert_type}({threat_category}.+?))\s*(\w+=|$)'] |
| added_regex_field | alert_type |  | ['\Wcat=({alert_type}({threat_category}.+?))\s*(\w+=|$)'] |
| added_regex_field | src_host |  | ['\Wdvchost=({src_host}({host}.+?))\s*(\w+=|$)', '\d\d:\d\d:\d\d\S+\s({src_host}({host}[\w\-\.]+))'] |
| removed_attribute | DupFields |  | N/A |
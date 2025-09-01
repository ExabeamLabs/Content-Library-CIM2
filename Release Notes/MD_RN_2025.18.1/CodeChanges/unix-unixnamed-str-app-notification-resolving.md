# Code Changes for unix-unixnamed-str-app-notification-resolving (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_port', 'dns_query', 'dns_query_type', 'event_name', 'host'] |
| removed_regex_field | dest_host |  | [] |
| edit_regex_field | dest_ip |  | ["({event_name}timed out resolving)\s+\'({dns_query}[^'\/]+?)\/({dns_query_type}[^'\/]+?)\/.*?\':\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\#({dest_port}\d+)"] |
| edit_regex_field | event_name |  | ["({event_name}timed out resolving)\s+\'({dns_query}[^'\/]+?)\/({dns_query_type}[^'\/]+?)\/.*?\':\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\#({dest_port}\d+)"] |
| added_regex_field | dest_port |  | ["({event_name}timed out resolving)\s+\'({dns_query}[^'\/]+?)\/({dns_query_type}[^'\/]+?)\/.*?\':\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\#({dest_port}\d+)"] |
| added_regex_field | dns_query |  | ["({event_name}timed out resolving)\s+\'({dns_query}[^'\/]+?)\/({dns_query_type}[^'\/]+?)\/.*?\':\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\#({dest_port}\d+)"] |
| added_regex_field | dns_query_type |  | ["({event_name}timed out resolving)\s+\'({dns_query}[^'\/]+?)\/({dns_query_type}[^'\/]+?)\/.*?\':\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\#({dest_port}\d+)"] |
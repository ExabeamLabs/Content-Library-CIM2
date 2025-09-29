# Code Changes for unix-unixnamed-str-network-notification-rfc1918 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dns_query', 'event_name', 'host', 'process_id', 'process_name', 'src_host', 'src_ip', 'src_port'] |
| removed_regex_field | dest_ip |  | [] |
| edit_regex_field | src_ip |  | ['client (@\dx[0-9a-fA-F]+)?\s*((({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-.]+))(#({src_port}\d+))?).+?Internet for ({dns_query}\S+)'] |
| added_regex_field | dns_query |  | ['client (@\dx[0-9a-fA-F]+)?\s*((({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-.]+))(#({src_port}\d+))?).+?Internet for ({dns_query}\S+)'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | src_host |  | ['client (@\dx[0-9a-fA-F]+)?\s*((({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-.]+))(#({src_port}\d+))?).+?Internet for ({dns_query}\S+)'] |
| added_regex_field | src_port |  | ['client (@\dx[0-9a-fA-F]+)?\s*((({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-.]+))(#({src_port}\d+))?).+?Internet for ({dns_query}\S+)'] |
| edit_attribute | activity_type |  | ['dns-request:success'] |
| edit_attribute | legacy_activity_type |  | ['dns-query'] |
| edit_attribute | legacy_product |  | ['DNS'] |
| edit_attribute | Platform |  | ['Unix Named'] |
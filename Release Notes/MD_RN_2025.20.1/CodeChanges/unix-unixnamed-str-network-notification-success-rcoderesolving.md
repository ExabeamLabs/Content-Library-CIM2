# Code Changes for unix-unixnamed-str-network-notification-success-rcoderesolving (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_port', 'dns_query', 'dns_query_type', 'event_name', 'host', 'result'] |
| removed_regex_field | dest_host |  | [] |
| edit_regex_field | dest_ip |  | [':\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(#?({dest_port}\d+))?'] |
| edit_regex_field | dest_port |  | [':\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(#?({dest_port}\d+))?'] |
| edit_regex_field | event_name |  | ["({result}\S+)\s+({event_name}unexpected RCODE resolving)\s+\'({dns_query}[^'\/]+?)\/({dns_query_type}[^'\/]+?)\/.*?\':"] |
| edit_regex_field | result |  | ["({result}\S+)\s+({event_name}unexpected RCODE resolving)\s+\'({dns_query}[^'\/]+?)\/({dns_query_type}[^'\/]+?)\/.*?\':"] |
| added_regex_field | dns_query |  | ["({result}\S+)\s+({event_name}unexpected RCODE resolving)\s+\'({dns_query}[^'\/]+?)\/({dns_query_type}[^'\/]+?)\/.*?\':"] |
| added_regex_field | dns_query_type |  | ["({result}\S+)\s+({event_name}unexpected RCODE resolving)\s+\'({dns_query}[^'\/]+?)\/({dns_query_type}[^'\/]+?)\/.*?\':"] |
| edit_attribute | activity_type |  | ['dns-request:fail'] |
| edit_attribute | legacy_activity_type |  | ['dns-query'] |
| edit_attribute | legacy_product |  | ['DNS'] |
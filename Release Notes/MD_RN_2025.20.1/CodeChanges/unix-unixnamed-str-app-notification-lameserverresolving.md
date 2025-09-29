# Code Changes for unix-unixnamed-str-app-notification-lameserverresolving (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_port', 'dns_query', 'event_name', 'host', 'process_id', 'process_name'] |
| removed_regex_field | dest_host |  | [] |
| edit_regex_field | dest_ip |  | [':\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(#?({dest_port}\d+))?'] |
| added_regex_field | dest_port |  | [':\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(#?({dest_port}\d+))?'] |
| added_regex_field | dns_query |  | ["lame server resolving \'({dns_query}[^']+?)\'"] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| edit_attribute | activity_type |  | ['dns-request:fail'] |
| edit_attribute | legacy_activity_type |  | ['dns-query'] |
| edit_attribute | legacy_product |  | ['DNS'] |
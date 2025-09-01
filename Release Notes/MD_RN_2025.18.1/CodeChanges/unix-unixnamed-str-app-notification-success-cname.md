# Code Changes for unix-unixnamed-str-app-notification-success-cname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dns_query', 'dns_query_type', 'event_name', 'host'] |
| edit_regex_field | dns_query |  | [": cname: ({event_name}.*?nameserver[^\']+?)\s*\'({dest_host}[\w\-\.]+?)\'.*?'({dns_query}[^\'\/]+)\/.*?({dns_query_type}[^\'\/]+)\'$"] |
| edit_regex_field | event_name |  | [": cname: ({event_name}.*?nameserver[^\']+?)\s*\'({dest_host}[\w\-\.]+?)\'.*?'({dns_query}[^\'\/]+)\/.*?({dns_query_type}[^\'\/]+)\'$"] |
| added_regex_field | dest_host |  | [": cname: ({event_name}.*?nameserver[^\']+?)\s*\'({dest_host}[\w\-\.]+?)\'.*?'({dns_query}[^\'\/]+)\/.*?({dns_query_type}[^\'\/]+)\'$"] |
| added_regex_field | dns_query_type |  | [": cname: ({event_name}.*?nameserver[^\']+?)\s*\'({dest_host}[\w\-\.]+?)\'.*?'({dns_query}[^\'\/]+)\/.*?({dns_query_type}[^\'\/]+)\'$"] |
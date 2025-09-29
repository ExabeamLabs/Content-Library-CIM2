# Code Changes for unix-unixnamed-str-dns-request-namedquery (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dns_query', 'dns_query_type', 'host', 'process_id', 'process_name', 'result', 'src_ip', 'src_port'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
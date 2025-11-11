# Code Changes for f5-bigipdns-str-dns-response-success-to (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_port', 'dns_query', 'dns_query_type', 'dns_response', 'dns_response_code', 'dns_response_flags', 'full_response', 'host', 'query_id', 'response_ttl', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | src_host |  | ['({time}\d\d\d\d-\d\d-\d\d (\d\d| \d):\d\d:\d\d)\s+({host}({src_host}[\w\.-]+))\s+qid'] |
| edit_regex_field | src_ip |  | ['({host}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?\s+qid', '\s({host}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?\s+qid'] |
| edit_regex_field | src_port |  | ['({host}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?\s+qid', '\s({host}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?\s+qid'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d\d-\d\d (\d\d| \d):\d\d:\d\d)\s+({host}({src_host}[\w\.-]+))\s+qid'] |
| added_regex_field | host |  | ['({host}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?\s+qid', '({time}\d\d\d\d-\d\d-\d\d (\d\d| \d):\d\d:\d\d)\s+({host}({src_host}[\w\.-]+))\s+qid', '\s({host}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?\s+qid'] |
| removed_attribute | DupFields |  | N/A |
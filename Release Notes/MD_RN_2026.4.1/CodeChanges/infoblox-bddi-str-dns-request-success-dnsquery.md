# Code Changes for infoblox-bddi-str-dns-request-success-dnsquery (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_ip', 'dest_port', 'dns_query', 'dns_query_type', 'dns_response', 'dns_response_code', 'dns_response_flags', 'host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | dest_ip |  | ['\d\d:\d\d:\d\d(\.\d+Z?)? (::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s'] |
| edit_regex_field | dest_port |  | ['\d\d:\d\d:\d\d(\.\d+Z?)? (::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s'] |
| removed_regex_field | dns_query_flags |  | [] |
| added_regex_field | dns_response |  | ['(\s+IN\s.+?){2}\s+\(?({dns_response}[^\s]+?)\s*(;|$|"|\.|\))\s*$'] |
| added_regex_field | dns_response_flags |  | ['\s+IN\s.+?\s+({dns_response_flags}[^\d\w].*?)\s'] |
| edit_attribute | Platform |  | ['Network', 'Unix'] |
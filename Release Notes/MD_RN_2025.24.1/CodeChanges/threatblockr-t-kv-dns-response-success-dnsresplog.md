# Code Changes for threatblockr-t-kv-dns-response-success-dnsresplog (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'dest_host', 'dest_ip', 'dest_port', 'dns_query', 'dns_query_type', 'protocol', 'response', 'result', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | action |  | ['\saction=({result}({action}[^=]+?))(,\s\w+=|\s*$)'] |
| added_regex_field | result |  | ['\saction=({result}({action}[^=]+?))(,\s\w+=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |
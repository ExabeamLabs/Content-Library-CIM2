# Code Changes for threatblockr-t-kv-network-traffic-packatlog (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'country', 'dest_host', 'dest_ip', 'dest_port', 'direction', 'group_name', 'protocol', 'result', 'rule', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | action |  | ['\saction=({result}({action}[^=]+?))(,\s\w+=|\s*$)'] |
| added_regex_field | result |  | ['\saction=({result}({action}[^=]+?))(,\s\w+=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for trendmicro-ds-cef-network-traffic-fail-idsdeny (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'bytes_in', 'bytes_out', 'dest_host', 'dest_ip', 'dest_mac', 'dest_port', 'failure_reason', 'file_dir', 'file_ext', 'file_hash', 'file_name', 'file_path', 'host', 'method', 'operation', 'protocol', 'rule', 'src_ip', 'src_mac', 'src_port', 'suid', 'user'] |
| edit_regex_field | rule |  | ['CEF.*?\|(.*?\|){4}({failure_reason}({rule}.+?))\|'] |
| added_regex_field | failure_reason |  | ['CEF.*?\|(.*?\|){4}({failure_reason}({rule}.+?))\|'] |
| removed_attribute | DupFields |  | N/A |
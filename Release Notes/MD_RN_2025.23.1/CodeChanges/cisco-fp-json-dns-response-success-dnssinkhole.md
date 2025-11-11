# Code Changes for cisco-fp-json-dns-response-success-dnssinkhole (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_type', 'bytes_in', 'bytes_out', 'dest_ip', 'dest_port', 'dns_query', 'dns_query_type', 'egress_interface', 'host', 'ingress_interface', 'protocol', 'result', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | alert_name |  | ['\sDNSSICategory:\s({alert_name}[^\s]+)'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for microsoft-evsecurity-json-endpoint-kerberosauth (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'result_code', 'service_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['"HostID":"({dest_host}({host}[^"]+))'] |
| added_regex_field | dest_host |  | ['"HostID":"({dest_host}({host}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |
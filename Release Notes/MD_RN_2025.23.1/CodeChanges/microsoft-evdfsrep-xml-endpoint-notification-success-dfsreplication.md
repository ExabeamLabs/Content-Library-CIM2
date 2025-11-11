# Code Changes for microsoft-evdfsrep-xml-endpoint-notification-success-dfsreplication (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'dest_host', 'event_code', 'event_id', 'host', 'process_guid', 'process_id', 'provider_name', 'result', 'result_code', 'run_level', 'sub_category', 'time'] |
| edit_regex_field | host |  | ['<Computer>({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | result |  | ['<Keywords>({result_code}({result}[^<]+))'] |
| added_regex_field | dest_host |  | ['<Computer>({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | result_code |  | ['<Keywords>({result_code}({result}[^<]+))'] |
| removed_attribute | DupFields |  | N/A |
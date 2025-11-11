# Code Changes for microsoft-evdirservice-xml-app-notification-success-directoryservice (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'domain', 'event_code', 'event_id', 'host', 'process_guid', 'process_id', 'provider_name', 'result', 'result_code', 'run_level', 'src_ip', 'src_port', 'sub_category', 'time', 'user', 'user_sid'] |
| edit_regex_field | result |  | ['<Keywords>({result_code}({result}[^<]+))'] |
| added_regex_field | result_code |  | ['<Keywords>({result_code}({result}[^<]+))'] |
| removed_attribute | DupFields |  | N/A |
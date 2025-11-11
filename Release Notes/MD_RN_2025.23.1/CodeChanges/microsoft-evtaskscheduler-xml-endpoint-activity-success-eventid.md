# Code Changes for microsoft-evtaskscheduler-xml-endpoint-activity-success-eventid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'client_name', 'error_code', 'event_code', 'event_id', 'event_name', 'host', 'process_guid', 'process_id', 'provider_name', 'result', 'result_code', 'run_level', 'sub_category', 'time', 'user_sid'] |
| edit_regex_field | result |  | ['<Keywords>({result_code}({result}[^<]+))'] |
| added_regex_field | result_code |  | ['<Keywords>({result_code}({result}[^<]+))'] |
| removed_attribute | DupFields |  | N/A |
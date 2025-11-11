# Code Changes for vmware-vcenter-str-endpoint-logout-success-loggedout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'domain', 'event_name', 'host', 'result', 'service_name', 'src_ip', 'time', 'user', 'user_agent'] |
| edit_regex_field | event_name |  | ['({result}({event_name}logged out))'] |
| added_regex_field | result |  | ['({result}({event_name}logged out))'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for citrix-cgateway-str-app-notification-trap_sent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'event_code', 'host', 'src_host', 'time'] |
| edit_regex_field | additional_info |  | ['GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*({event_code}(\w+\s+){2}\w+)\s+[^:]+:\s*"*({additional_info}[^)]+\)?)', 'GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*({event_code}(\w+\s+){3})[^:]+:\s*"*({additional_info}[^)]+)'] |
| edit_regex_field | event_code |  | ['GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*({event_code}(\w+\s+){2}\w+)\s+[^:]+:\s*"*({additional_info}[^)]+\)?)', 'GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*({event_code}(\w+\s+){3})[^:]+:\s*"*({additional_info}[^)]+)'] |
| edit_regex_field | host |  | ['GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*({event_code}(\w+\s+){2}\w+)\s+[^:]+:\s*"*({additional_info}[^)]+\)?)', 'GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*({event_code}(\w+\s+){3})[^:]+:\s*"*({additional_info}[^)]+)'] |
| added_regex_field | src_host |  | ['GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*({event_code}(\w+\s+){2}\w+)\s+[^:]+:\s*"*({additional_info}[^)]+\)?)', 'GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*({event_code}(\w+\s+){3})[^:]+:\s*"*({additional_info}[^)]+)'] |
| removed_attribute | DupFields |  | N/A |
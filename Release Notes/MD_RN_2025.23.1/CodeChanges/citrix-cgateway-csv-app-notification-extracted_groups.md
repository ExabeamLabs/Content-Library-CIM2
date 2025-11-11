# Code Changes for citrix-cgateway-csv-app-notification-extracted_groups (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_name', 'host', 'src_host', 'time'] |
| edit_regex_field | event_name |  | ['GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+){2})[^:]+:\s*Extracted_groups\s+', 'GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+\w+))[^:]+:\s*Extracted_groups\s+'] |
| edit_regex_field | host |  | ['GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+){2})[^:]+:\s*Extracted_groups\s+', 'GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+\w+))[^:]+:\s*Extracted_groups\s+'] |
| added_regex_field | src_host |  | ['GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+){2})[^:]+:\s*Extracted_groups\s+', 'GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+\w+))[^:]+:\s*Extracted_groups\s+'] |
| removed_attribute | DupFields |  | N/A |
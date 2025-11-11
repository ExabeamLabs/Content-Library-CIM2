# Code Changes for citrix-cgateway-kv-app-notification-monitorup (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'event_name', 'host', 'src_host', 'time'] |
| edit_regex_field | additional_info |  | ['GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+){2})[^:]+:\s*({additional_info}[^"]+)"*', 'GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+\w+))[^:]+:\s*({additional_info}.+?)\s+($|")'] |
| edit_regex_field | event_name |  | ['({event_name}EVENT MONITORUP)', 'GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+){2})[^:]+:\s*({additional_info}[^"]+)"*', 'GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+\w+))[^:]+:\s*({additional_info}.+?)\s+($|")'] |
| edit_regex_field | host |  | ['GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+){2})[^:]+:\s*({additional_info}[^"]+)"*', 'GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+\w+))[^:]+:\s*({additional_info}.+?)\s+($|")'] |
| added_regex_field | src_host |  | ['GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+){2})[^:]+:\s*({additional_info}[^"]+)"*', 'GMT\s*({src_host}({host}[^:\s]+))(\s\S+)?\s:\s*\w+\s*({event_name}(\w+\s+\w+))[^:]+:\s*({additional_info}.+?)\s+($|")'] |
| removed_attribute | DupFields |  | N/A |
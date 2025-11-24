# Code Changes for unix-events-1 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'host', 'time'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d(\.\S+)? \d\d\d\d ({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['\d\d:\d\d:\d\d(\.\S+)? \d\d\d\d ({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |
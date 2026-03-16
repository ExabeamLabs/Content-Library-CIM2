# Code Changes for barracuda-waf-str-app-notification-samltokenparsed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'host', 'time'] |
| added_regex_field | host |  | ['\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d+\s*(\+|\-)[\d:]+\s({host}[\w\-.]+)\s'] |
# Code Changes for trendmicro-ddi-kv-alert-trigger-alertevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'event_name', 'host', 'host_ip', 'time'] |
| edit_regex_field | host |  | ['({host}[\w.\-]+)\s+CEF:([^\|]*\|){5}({alert_name}[^\|]+)', '({host}[\w.\-]+)\s+CEF:([^\|]*\|){5}({event_name}[^\|]+)', '\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)'] |
| added_regex_field | alert_name |  | ['({host}[\w.\-]+)\s+CEF:([^\|]*\|){5}({alert_name}[^\|]+)'] |
| removed_attribute | DupFields |  | N/A |
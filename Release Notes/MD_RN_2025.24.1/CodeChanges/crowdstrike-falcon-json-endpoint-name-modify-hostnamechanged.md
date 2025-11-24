# Code Changes for crowdstrike-falcon-json-endpoint-name-modify-hostnamechanged (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['aid', 'event_code', 'event_name', 'host', 'os', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | event_name |  | ['"event_simpleName":"({event_code}({event_name}[^"]+)'] |
| added_regex_field | event_code |  | ['"event_simpleName":"({event_code}({event_name}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |
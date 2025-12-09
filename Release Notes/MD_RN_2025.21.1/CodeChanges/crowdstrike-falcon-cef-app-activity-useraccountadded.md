# Code Changes for crowdstrike-falcon-cef-app-activity-useraccountadded (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['aid', 'aip', 'cid', 'email_address', 'email_domain', 'event_code', 'operation', 'os', 'result', 'src_port', 'time', 'user'] |
| added_regex_field | event_code |  | ['"event_simpleName":"({event_code}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |
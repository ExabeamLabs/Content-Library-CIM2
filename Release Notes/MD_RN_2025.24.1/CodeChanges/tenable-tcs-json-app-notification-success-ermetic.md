# Code Changes for tenable-tcs-json-app-notification-success-ermetic (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'account_name', 'additional_info', 'app', 'description', 'event_name', 'event_subtype', 'link', 'log_source', 'severity', 'status_msg', 'time'] |
| edit_regex_field | log_source |  | ['"source":\s*"({app}({log_source}[^"]+))"'] |
| added_regex_field | app |  | ['"source":\s*"({app}({log_source}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for mcafee-sncasb-cef-file-download-success-anomalousaccesslocation (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'email_address', 'email_domain', 'event_name', 'host', 'operation', 'time', 'user'] |
| edit_regex_field | event_name |  | ['({operation}({event_name}File downloaded))'] |
| added_regex_field | operation |  | ['({operation}({event_name}File downloaded))'] |
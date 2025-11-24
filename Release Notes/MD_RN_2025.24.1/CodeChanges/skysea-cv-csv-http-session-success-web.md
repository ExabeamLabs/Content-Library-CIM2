# Code Changes for skysea-cv-csv-http-session-success-web (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'dest_port', 'host', 'method', 'protocol', 'src_host', 'src_ip', 'src_port', 'time', 'uri_path', 'uri_query', 'url', 'user', 'web_domain'] |
| edit_regex_field | action |  | ['({method}({action}Web書き込み))'] |
| added_regex_field | method |  | ['({method}({action}Web書き込み))'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for imperva-incapsula-cef-http-session-siemintegration (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'attack', 'bytes', 'city', 'country_code', 'dest_ip', 'dest_port', 'file_type', 'http_response_code', 'method', 'permission', 'protocol', 'rule', 'src_ip', 'src_port', 'time', 'uri_path', 'uri_query', 'url', 'user_agent', 'web_domain'] |
| edit_regex_field | uri_path |  | ['request\\?=({url}({uri_path}[^\s]+))\s'] |
| added_regex_field | url |  | ['request\\?=({url}({uri_path}[^\s]+))\s'] |
| removed_attribute | DupFields |  | N/A |
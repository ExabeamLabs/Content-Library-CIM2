# Code Changes for imperva-incapsula-leef-http-session-siemintegration (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'app', 'categories', 'category', 'client_id', 'country_code', 'dest_ip', 'dest_port', 'host', 'http_response_code', 'method', 'protocol', 'referrer', 'src_ip', 'src_port', 'time', 'uri_path', 'uri_query', 'url', 'user_agent', 'web_domain'] |
| removed_regex_field | site_id |  | [] |
| added_regex_field | client_id |  | ['siteid=({client_id}\d+)'] |
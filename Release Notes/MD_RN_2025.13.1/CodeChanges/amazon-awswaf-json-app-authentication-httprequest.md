# Code Changes for amazon-awswaf-json-app-authentication-httprequest (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'action', 'aws_account', 'browser', 'http_response_code', 'method', 'os', 'referrer', 'rule', 'rule_id', 'src_ip', 'src_port', 'time', 'uri_path', 'user_agent', 'web_domain'] |
| removed_regex_field | top_domain |  | [] |
| edit_regex_field | web_domain |  | ['"name"+:"+(?i)Host"+,"+value"+:"+({web_domain}[^="]+?)[\\\/\s:"]', 'exa_json_path=$.httpRequest.headers[?(@.name == \'Host\')].value,exa_regex=({web_domain}[^="]+?)[\\\/\s:"]'] |
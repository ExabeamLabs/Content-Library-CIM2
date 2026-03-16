# Code Changes for akamai-siem-json-http-session-httpmessage (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['src_ip', 'src_port', 'user_agent'] |
| added_regex_field | user_agent |  | ['exa_json_path=$.updatedhttpMessage.requestHeaders.User-Agent,exa_regex=\s*({user_agent}[^"$]+)'] |
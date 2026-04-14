# Code Changes for crowdstrike-falcon-json-app-login-apiactivityauditevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['email_address', 'email_domain', 'http_response_code', 'src_ip', 'src_port', 'user'] |
| added_regex_field | http_response_code |  | ['exa_json_path=$.event..status_code,exa_regex=({http_response_code}\d+)'] |
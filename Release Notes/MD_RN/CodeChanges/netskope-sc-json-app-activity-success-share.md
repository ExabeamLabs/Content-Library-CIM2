# Code Changes for netskope-sc-json-app-activity-success-share (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'src_ip', 'src_port', 'uri_path', 'uri_query', 'url', 'user', 'web_domain'] | ['dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'src_ip', 'src_port', 'time', 'uri_path', 'uri_query', 'url', 'user', 'web_domain'] |
| added_regex_field | time | [] | ['exa_json_path=$.timestamp,exa_regex=({time}\d{10})'] |
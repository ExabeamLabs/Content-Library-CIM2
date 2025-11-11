# Code Changes for microsoft-evsecurity-json-user-delete-fail-user (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | src_domain |  | ['"DomainID":"({domain}({src_domain}[^\"]+))'] |
| added_regex_field | domain |  | ['"DomainID":"({domain}({src_domain}[^\"]+))'] |
| removed_attribute | DupFields |  | N/A |
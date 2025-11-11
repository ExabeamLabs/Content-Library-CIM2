# Code Changes for json-windows-events-4 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'login_id', 'src_domain', 'time', 'user_sid'] |
| edit_regex_field | domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))"'] |
| removed_regex_field | src_ip |  | [] |
| removed_regex_field | src_port |  | [] |
| removed_regex_field | user |  | [] |
| added_regex_field | src_domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |
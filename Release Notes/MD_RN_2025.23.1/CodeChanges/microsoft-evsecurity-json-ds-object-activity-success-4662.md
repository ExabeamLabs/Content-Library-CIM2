# Code Changes for microsoft-evsecurity-json-ds-object-activity-success-4662 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'additional_info', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object', 'object_name', 'object_server', 'object_type', 'operation', 'properties', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))"'] |
| edit_regex_field | object_name |  | ['"ObjectName":"({object}({object_name}[^"]+))"'] |
| edit_regex_field | user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | object |  | ['"ObjectName":"({object}({object_name}[^"]+))"'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))"'] |
| added_regex_field | src_user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| removed_attribute | DupFields |  | N/A |
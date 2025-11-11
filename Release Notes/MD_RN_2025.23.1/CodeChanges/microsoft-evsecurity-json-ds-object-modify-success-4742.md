# Code Changes for microsoft-evsecurity-json-ds-object-modify-success-4742 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['attribute', 'dest_host', 'dest_user', 'domain', 'ds_object_dn', 'event_code', 'event_name', 'host', 'login_id', 'new_value', 'old_value', 'src_domain', 'src_host', 'src_user', 'time', 'uac_status', 'user'] |
| edit_regex_field | domain |  | ['SubjectDomainName"\s*:\s*"({src_domain}({domain}[^"]+))'] |
| edit_regex_field | host |  | ['"(?:winlog\.)?computer_name"\s*:\s*"({dest_host}({host}[\w\-.]+?))"'] |
| edit_regex_field | user |  | ['SubjectUserName"\s*:\s*"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | dest_host |  | ['"(?:winlog\.)?computer_name"\s*:\s*"({dest_host}({host}[\w\-.]+?))"'] |
| added_regex_field | src_domain |  | ['SubjectDomainName"\s*:\s*"({src_domain}({domain}[^"]+))'] |
| added_regex_field | src_user |  | ['SubjectUserName"\s*:\s*"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |
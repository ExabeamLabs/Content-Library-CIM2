# Code Changes for microsoft-evsecurity-xml-member-remove-success-4762 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | account_id |  | ['<\/Data><Data Name=(\'|")MemberSid(\'|")>(({dest_user_sid}S-\d+-[^<]+)|({account_id}[^<]+))<'] |
| edit_regex_field | dest_user_sid |  | ['<\/Data><Data Name=(\'|")MemberSid(\'|")>(({dest_user_sid}S-\d+-[^<]+)|({account_id}[^<]+))<'] |
| edit_regex_field | provider_name |  | ['<Provider>({provider_name}.+?)</Provider>', 'Provider Name:\s*({provider_name}.+?)\s+Algorithm Name:', 'Provider Name\\*=(\'|")({provider_name}[^\\'"]+)', 'Provider Name\\*=(\'|")({provider_name}[^\\'"]+)'] |
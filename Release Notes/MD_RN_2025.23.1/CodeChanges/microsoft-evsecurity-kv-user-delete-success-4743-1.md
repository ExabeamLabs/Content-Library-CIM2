# Code Changes for microsoft-evsecurity-kv-user-delete-success-4743-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object', 'object_dn', 'time', 'user', 'user_sid'] |
| edit_regex_field | dest_user |  | ['Target Computer:\s+Security ID:\s+(NT AUTHORITY\\(SYSTEM|LOCAL SERVICE)|({dest_user_sid}[^:]+?))\s+Account Name:\s+(?=\w)({object}({account_name}({dest_user}[^:]+?)))\s+Account Domain:\s+(?=\w)({object_dn}[^:]+?)\s+Additional Information:'] |
| edit_regex_field | dest_user_sid |  | ['Target Computer:\s+Security ID:\s+(NT AUTHORITY\\(SYSTEM|LOCAL SERVICE)|({dest_user_sid}[^:]+?))\s+Account Name:\s+(?=\w)({object}({account_name}({dest_user}[^:]+?)))\s+Account Domain:\s+(?=\w)({object_dn}[^:]+?)\s+Additional Information:'] |
| edit_regex_field | object_dn |  | ['Target Computer:\s+Security ID:\s+(NT AUTHORITY\\(SYSTEM|LOCAL SERVICE)|({dest_user_sid}[^:]+?))\s+Account Name:\s+(?=\w)({object}({account_name}({dest_user}[^:]+?)))\s+Account Domain:\s+(?=\w)({object_dn}[^:]+?)\s+Additional Information:'] |
| added_regex_field | account_name |  | ['Target Computer:\s+Security ID:\s+(NT AUTHORITY\\(SYSTEM|LOCAL SERVICE)|({dest_user_sid}[^:]+?))\s+Account Name:\s+(?=\w)({object}({account_name}({dest_user}[^:]+?)))\s+Account Domain:\s+(?=\w)({object_dn}[^:]+?)\s+Additional Information:'] |
| added_regex_field | object |  | ['Target Computer:\s+Security ID:\s+(NT AUTHORITY\\(SYSTEM|LOCAL SERVICE)|({dest_user_sid}[^:]+?))\s+Account Name:\s+(?=\w)({object}({account_name}({dest_user}[^:]+?)))\s+Account Domain:\s+(?=\w)({object_dn}[^:]+?)\s+Additional Information:'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for microsoft-evntlm-xml-endpoint-login-fail-8004 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'policy_name', 'process_id', 'resource', 'run_level', 'src_host', 'time', 'user', 'user_sid', 'user_upn'] |
| edit_regex_field | resource |  | ['Name=(\'|")SChannelName(\'|")>({dest_host}({resource}[^<>]+))<'] |
| added_regex_field | dest_host |  | ['Name=(\'|")SChannelName(\'|")>({dest_host}({resource}[^<>]+))<'] |
| removed_attribute | DupFields |  | N/A |
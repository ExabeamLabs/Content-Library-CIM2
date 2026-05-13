# Code Changes for github-g-json-app-activity-success-workflowscompletedworkflowrun (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'company', 'domain', 'email_address', 'key_name', 'object', 'operation', 'operation_type', 'protocol', 'repository_name', 'src_ip', 'src_port', 'time', 'user', 'user_agent', 'user_id'] |
| added_regex_field | user_id |  | ['"actor_id":\s*({user_id}[^",]+)'] |
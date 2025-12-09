# Code Changes for github-g-json-app-activity-success-preparedworkflowjob (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'company', 'domain', 'email_address', 'key_name', 'object', 'operation', 'operation_type', 'protocol', 'repository_name', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| edit_regex_field | object |  | ['"job_workflow_ref":"({repository_name}({object}[^"]+))', '"repo":\s*"({repository_name}({object}[^"]+))'] |
| added_regex_field | repository_name |  | ['"job_workflow_ref":"({repository_name}({object}[^"]+))', '"repo":\s*"({repository_name}({object}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |
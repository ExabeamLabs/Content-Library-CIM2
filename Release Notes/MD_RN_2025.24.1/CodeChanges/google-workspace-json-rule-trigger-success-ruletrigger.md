# Code Changes for google-workspace-json-rule-trigger-success-ruletrigger (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'app', 'email_address', 'email_domain', 'operation', 'recipients', 'resource_id', 'resource_name', 'resource_path', 'resource_type', 'rule', 'rule_severity', 'rule_source', 'rule_type', 'scan_type', 'time', 'user', 'user_id'] |
| edit_regex_field | rule_source |  | ['"data_source"[^}]+?"value":"({app}({rule_source}[^"]+))"'] |
| added_regex_field | app |  | ['"data_source"[^}]+?"value":"({app}({rule_source}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |
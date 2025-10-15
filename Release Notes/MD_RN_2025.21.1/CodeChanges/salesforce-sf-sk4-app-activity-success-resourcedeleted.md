# Code Changes for salesforce-sf-sk4-app-activity-success-resourcedeleted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'dest_email_address', 'dest_email_domain', 'dest_user', 'email_address', 'email_domain', 'first_name', 'full_name', 'last_name', 'object', 'operation', 'resource', 'time', 'user'] |
| edit_regex_field | object |  | ['fname=({resource}({object}.+?))\s+(\w+=|$)'] |
| added_regex_field | resource |  | ['fname=({resource}({object}.+?))\s+(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |
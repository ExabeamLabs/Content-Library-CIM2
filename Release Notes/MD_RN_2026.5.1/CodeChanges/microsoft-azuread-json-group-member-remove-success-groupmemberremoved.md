# Code Changes for microsoft-azuread-json-group-member-remove-success-groupmemberremoved (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'app', 'category', 'email_address', 'email_domain', 'event_name', 'group_name', 'operation', 'result', 'src_ip', 'src_port', 'tenant_id', 'time', 'user_uid'] |
| edit_regex_field | app |  | ['"app":\{[^\}]+displayName":"({app}[^"]+)"', '"loggedByService":"({app}[^"]+)"'] |
| edit_regex_field | category |  | ['"category":"({category}[^"]+)'] |
| edit_regex_field | operation |  | ['"operationName":"({operation}[^"]+)"'] |
| edit_regex_field | result |  | ['"result":"(notEnabled|notApplied|({result}[^",]+))'] |
| edit_regex_field | user_uid |  | ['"targetResources":[^\}]+"id":"({user_uid}[^",]+)'] |
| added_regex_field | tenant_id |  | ['"TenantId":\s*"({tenant_id}[^"]+)"'] |
# Code Changes for microsoft-azure-json-group-member-remove-success-removefromgroup (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['additional_info', 'app', 'category', 'correlation_id', 'dest_email_address', 'dest_email_domain', 'dest_user', 'email_address', 'email_domain', 'event_name', 'group_name', 'operation', 'result', 'result_reason', 'src_ip', 'src_port', 'time', 'user_uid'] | ['additional_info', 'app', 'category', 'correlation_id', 'dest_email_address', 'dest_email_domain', 'dest_user', 'email_address', 'email_domain', 'event_name', 'group_name', 'operation', 'result', 'result_reason', 'service_name', 'src_ip', 'src_port', 'target', 'time', 'user_uid'] |
| edit_regex_field | app | ['"initiatedBy":\s*\{"app":\s*\{[^\}]*?"displayName":\s*"({app}[^"]+)"', '"loggedByService":\s*"(Account Provisioning|Core Directory|({app}[^"]+))"'] | ['"app":\s*\{[^\}]*?"displayName":\s*"({app}[^"]+)"', '"loggedByService":\s*"(Account Provisioning|Core Directory|({app}[^"]+))"'] |
| added_regex_field | service_name | [] | ['"loggedByService":\s*"({service_name}[^"]+)"'] |
| added_regex_field | target | [] | ['"targetResources"+:\[[^\]]+?"+displayName"+:"+({target}[^"]+?)\s*"'] |
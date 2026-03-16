# Code Changes for microsoft-azuremon-sk4-app-activity-success-updategroup (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'dest_email_address', 'dest_email_domain', 'dest_user', 'email_address', 'event_category', 'event_name', 'failure_reason', 'group_name', 'object', 'operation', 'provider_name', 'resource', 'resource_group', 'resource_id', 'result', 'src_ip', 'subscription_id', 'time', 'user_agent'] |
| edit_regex_field | additional_info |  | ['"modifiedProperties":\s*\[\s*({additional_info}.+?)](,|$)', '"type":\s*"({additional_info}[^"]+)'] |
| edit_regex_field | email_address |  | ['"InitiatedBy(\_dynamic)?":\s*"?\{\\?"user\\?":\s*\{[^\}]+"userPrincipalName\\?":\s*\\?"({email_address}[^@"]+@[^\."]+\.[^"]+?)\\?"'] |
| edit_regex_field | src_ip |  | ['"InitiatedBy(\_dynamic)?":\s*"?\{\\?"user\\?":\s*\{[^\}]+"ipAddress\\?":\s*\\?"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)\\?"', 'CallerIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"'] |
| added_regex_field | group_name |  | ['"TargetResources":\s*"?\[[^|\]]+?"displayName":"({group_name}[^"]+)[^|\[\]\{\}]+?"type":"Group"'] |
| edit_attribute | activity_type |  | ['group-modify:fail', 'group-modify:success', 'key-read:fail', 'key-read:success'] |
# Code Changes for m365-activity (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'app_id', 'email_subject', 'file_name', 'group_name', 'login_type', 'object', 'object_type', 'operation', 'owner', 'process_name', 'result', 'session_id', 'tenant_id', 'time', 'user_agent', 'user_type', 'user_upn'] |
| added_regex_field | owner |  | ['"MailboxOwnerUPN":"({owner}[^"]+)"'] |
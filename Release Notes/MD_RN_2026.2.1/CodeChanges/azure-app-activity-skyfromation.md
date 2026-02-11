# Code Changes for azure-app-activity-skyfromation (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'account_name', 'action', 'additional_info', 'aio', 'app', 'app_id', 'app_id_acr', 'app_module', 'aud', 'category', 'channels', 'correlation_id', 'email_address', 'endpoint', 'error_code', 'event_id', 'event_name', 'exp', 'iat', 'iss', 'method', 'nbf', 'object', 'operation', 'resource', 'resource_group', 'resource_id', 'result', 'scope', 'service_request_id', 'src_ip', 'src_port', 'subscription_id', 'tenant_id', 'time', 'user', 'user_id', 'uti', 'version', 'xms_mirid'] |
| removed_regex_field | event_code |  | [] |
| added_regex_field | event_id |  | ['"+src-event-id"+:"+({event_id}[^"]+)'] |
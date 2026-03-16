# Code Changes for microsoft-azuremon-sk4-secret-read-getsecret (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'browser', 'category', 'correlation_id', 'email_address', 'event_hub_name', 'event_hub_namespace', 'full_name', 'host', 'http_response_code', 'object', 'operation', 'os', 'resource', 'src_ip', 'src_port', 'time', 'user_agent', 'user_type', 'user_upn'] |
| edit_regex_field | email_address |  | ['"email":"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)', 'claims\/(name|upn)":\s*"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)'] |
| removed_regex_field | email_domain |  | [] |
# Code Changes for microsoft-azureeh-csv-alert-trigger-security (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'app', 'azure_resource_type', 'category', 'email_address', 'event_hub_name', 'event_hub_namespace', 'full_name', 'host', 'last_known_ip', 'location', 'object', 'operation', 'provider_name', 'resource', 'resource_group', 'resource_id', 'result_code', 'server_name', 'severity', 'src_ip', 'src_port', 'subscription_id', 'time', 'user', 'user_agent', 'user_upn'] |
| edit_regex_field | email_address |  | ['"Caller":"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"', '"email":"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)', 'claims\/(name|upn)":\s*"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)', 'exa_json_path=$.Caller,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)', 'userId":"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)'] |
| removed_regex_field | email_domain |  | [] |
| removed_regex_field | user_id |  | [] |
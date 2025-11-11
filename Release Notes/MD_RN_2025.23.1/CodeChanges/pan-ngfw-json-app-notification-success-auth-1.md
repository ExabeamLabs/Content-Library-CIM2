# Code Changes for pan-ngfw-json-app-notification-success-auth-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['email_address', 'email_domain', 'event_category', 'firewall', 'host', 'operation', 'src_ip'] |
| added_regex_field | firewall |  | ['exa_json_path=$..DeviceName,exa_regex=^({firewall}[\w.-]+)', 'exa_json_path=$.LogSourceName,exa_regex=^({firewall}[\w.-]+)$', 'exa_json_path=$.event.LogSourceName,exa_regex=^({firewall}[\w.-]+)$'] |
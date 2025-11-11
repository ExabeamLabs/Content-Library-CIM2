# Code Changes for pan-ngfw-json-endpoint-authentication-fail-authfail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'email_address', 'email_domain', 'event_category', 'firewall', 'host', 'src_ip', 'src_port', 'user'] |
| added_regex_field | firewall |  | ['exa_json_path=$..DeviceName,exa_regex=^({firewall}[\w.-]+)', 'exa_json_path=$.LogSourceName,exa_regex=^({firewall}[\w.-]+)$', 'exa_json_path=$.event.LogSourceName,exa_regex=^({firewall}[\w.-]+)$'] |
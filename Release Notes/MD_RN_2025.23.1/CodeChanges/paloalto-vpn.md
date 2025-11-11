# Code Changes for paloalto-vpn (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'dest_ip', 'dest_translated_ip', 'domain', 'email_address', 'firewall', 'host', 'src_ip', 'src_port', 'src_translated_ip', 'threat_category', 'time', 'user'] |
| added_regex_field | firewall |  | ['exa_json_path=$.DeviceName,exa_regex=^({firewall}[\w.-]+)$', 'exa_json_path=$.event.DeviceName,exa_regex=^({firewall}[\w.-]+)$', 'exa_json_path=$.event.host,exa_regex=^({firewall}[\w.-]+)$', 'exa_json_path=$.host,exa_regex=^({firewall}[\w.-]+)$'] |
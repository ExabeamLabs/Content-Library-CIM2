# Code Changes for symantec-endpointprotection-json-alert-trigger-success-firewallnetworkdetection (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | attack_info | ['"attacks":\[({attack_info}.+?\})\]', 'exa_json_path=$.attacks,exa_field_name=:\[({attack_info}.+?\})\]'] | ['"attacks":\[({attack_info}.+?\})\]', 'exa_json_path=$.attacks,exa_regex=\[({attack_info}.+?\})\]'] |
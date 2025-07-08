# Code Changes for symantec-endpointprotection-json-alert-trigger-success-firewallnetworkdetection (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | attack_info | ['"attacks":\[({attack_info}.+?\})\]', 'exa_json_path=$.attacks,exa_field_name=:\[({attack_info}.+?\})\]'] | ['"attacks":\[({attack_info}.+?\})\]', 'exa_json_path=$.attacks,exa_regex=\[({attack_info}.+?\})\]'] |
# Code Changes for pingidentity-pi-json-vpn-authentication-success-pingid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'app_id', 'browser', 'device_name', 'email_address', 'mfa_country', 'mfa_device', 'os', 'policy_name', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| edit_regex_field | device_name |  | ['Device Model:\s*(N\/A|({mfa_device}({device_name}[^:]+?)))(\\?[\sn])Device Lock Enabled:'] |
| added_regex_field | mfa_device |  | ['Device Model:\s*(N\/A|({mfa_device}({device_name}[^:]+?)))(\\?[\sn])Device Lock Enabled:'] |
| removed_attribute | DupFields |  | N/A |
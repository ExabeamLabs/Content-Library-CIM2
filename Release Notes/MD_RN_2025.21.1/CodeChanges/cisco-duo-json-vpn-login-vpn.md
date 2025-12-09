# Code Changes for cisco-duo-json-vpn-login-vpn (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['browser', 'browser_version', 'domain', 'email_address', 'email_domain', 'event_name', 'factor', 'failure_reason', 'host', 'mfa_country', 'mfa_device', 'os', 'os_version', 'result', 'service_name', 'src_country', 'src_ip', 'time', 'user'] |
| edit_regex_field | src_country |  | ['"location":.+?"country":\s*"({mfa_country}({src_country}[^"]+))'] |
| added_regex_field | mfa_country |  | ['"location":.+?"country":\s*"({mfa_country}({src_country}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |
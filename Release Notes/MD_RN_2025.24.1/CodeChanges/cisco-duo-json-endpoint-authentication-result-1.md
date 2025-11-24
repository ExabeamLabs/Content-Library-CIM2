# Code Changes for cisco-duo-json-endpoint-authentication-result-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'browser', 'browser_version', 'domain', 'email_address', 'email_domain', 'factor', 'failure_reason', 'host', 'mfa_country', 'mfa_device', 'os', 'os_version', 'result_reason', 'service_name', 'src_country', 'src_ip', 'time', 'user'] |
| edit_regex_field | src_ip |  | ['"ip":"+(0.0.0.0|null|({src_ip}[a-fA-F:\.\d]+))"'] |
| removed_regex_field | src_port |  | [] |
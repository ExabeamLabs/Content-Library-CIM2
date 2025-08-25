# Code Changes for cisco-duo-json-endpoint-authentication-result-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'browser', 'browser_version', 'domain', 'email_address', 'email_domain', 'factor', 'failure_reason', 'host', 'mfa_country', 'mfa_device', 'os', 'os_version', 'result_reason', 'service_name', 'src_country', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | result_reason |  | ['"reason":"({result_reason}[^"]+)"[^=]+?"result":"success"', '"result":"success"[^=]+?"reason":"({result_reason}[^"]+)"'] |
# Code Changes for cisco-duo-json-endpoint-authentication-result-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'browser', 'browser_version', 'city', 'domain', 'email_address', 'email_domain', 'factor', 'failure_reason', 'host', 'location_city', 'location_state', 'mfa_country', 'mfa_device', 'os', 'os_version', 'result_reason', 'service_name', 'src_country', 'src_ip', 'src_port', 'state', 'time', 'user'] |
| added_regex_field | city |  | ['"access_device":\{.*?"location":\{[^\}]*?"city":"(null|({city}[^"]+))"'] |
| added_regex_field | location_city |  | ['"auth_device":\{.*?"location":\{[^\}]*?"city":"(null|({location_city}[^"]+))"'] |
| added_regex_field | location_state |  | ['"auth_device":\{.*?"location":\{[^\}]*?"state":"(null|({location_state}[^"]+))"'] |
| added_regex_field | state |  | ['"access_device":\{.*?"location":\{[^\}]*?"state":"(null|({state}[^"]+))"'] |
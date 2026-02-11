# Code Changes for citrix-sharefile-sk4-app-login-success-loginactivity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'company', 'country_code', 'email_address', 'email_domain', 'event_id', 'full_name', 'operation', 'src_ip', 'src_port', 'time', 'uri_path'] |
| removed_regex_field | event_code |  | [] |
| added_regex_field | event_id |  | ['"+EventID"+:"+({event_id}[^"]+)"+'] |
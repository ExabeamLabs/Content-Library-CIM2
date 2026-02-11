# Code Changes for auth0-a-json-app-authentication-fail-gd_auth_failed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_severity', 'app', 'auth_type', 'domain', 'email_address', 'host', 'operation_type', 'src_ip', 'src_port', 'time', 'user_agent', 'user_id'] |
| edit_regex_field | email_address |  | ['exa_json_path=$..user_name,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)', 'exa_json_path=$.data..user.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)', 'exa_regex="user_name":"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)', 'user_name"+:"+({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"'] |
| removed_regex_field | email_domain |  | [] |
| removed_regex_field | user |  | [] |
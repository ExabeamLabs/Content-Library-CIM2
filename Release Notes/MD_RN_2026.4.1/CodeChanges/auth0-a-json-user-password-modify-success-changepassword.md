# Code Changes for auth0-a-json-user-password-modify-success-changepassword (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_severity', 'app', 'auth_type', 'confidence_level', 'domain', 'email_address', 'host', 'operation_type', 'src_ip', 'src_port', 'time', 'user_agent', 'user_id'] |
| edit_regex_field | email_address |  | ['(user_name|userEmail)\\?"+:\\?"+({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)', 'exa_json_path=$..user_name,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)', 'exa_json_path=$.data..user.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)', 'exa_regex=(user_name|userEmail)\\?"+:\\?"+({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)'] |
| added_regex_field | confidence_level |  | ['"riskAssessment":[^\}]+?"confidence":"({confidence_level}[^"]+)"'] |
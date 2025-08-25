# Code Changes for microsoft-m365auditlogs-json-app-activity-operationname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'attribute', 'category', 'correlation_id', 'dest_host', 'email_address', 'email_domain', 'error_code', 'full_name', 'host', 'object', 'operation', 'principal_id', 'result', 'result_reason', 'src_ip', 'src_port', 'tenant_id', 'time', 'user', 'user_uid'] |
| edit_regex_field | app |  | ['"?loggedByService":\s*"(?:Account Provisioning|Core Directory|({app}[^",]+))"?', '"app":\{.*?displayName":"({app}[^",]+)', '"category":"(?!RiskyUsers|UserRiskEvents|ProvisioningLogs)[^"]+"[^=]+?"identity":"({app}[^"]+)"', '"identity":"({app}[^"]+)"[^=]+?"category":"(?!RiskyUsers|UserRiskEvents|ProvisioningLogs)[^"]+"'] |
| edit_regex_field | category |  | ['"?category":"({category}[^",]+)'] |
| edit_regex_field | email_address |  | ['"userPrincipalName":"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_domain |  | ['"userPrincipalName":"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | time |  | ['"?time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}Z)', '"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\dZ)"', '"time":"({time}\d{1,2}\/\d{1,2}\/\d{4} \d{2}:\d{2}:\d{2} (?:AM|PM))'] |
| added_regex_field | full_name |  | ['"category":"(?:RiskyUsers|UserRiskEvents)"[^=]+?"identity":"(?:({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"]+))"', '"identity":"(?:({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"]+))"[^=]+?"category":"(?:RiskyUsers|UserRiskEvents)"'] |
| added_regex_field | user |  | ['"category":"(?:RiskyUsers|UserRiskEvents)"[^=]+?"identity":"(?:({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"]+))"', '"identity":"(?:({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"]+))"[^=]+?"category":"(?:RiskyUsers|UserRiskEvents)"'] |
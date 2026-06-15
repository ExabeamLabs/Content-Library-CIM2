# Code Changes for zscaler-ia-json-alert-trigger-success-zscalernsscasbsecurityfile (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_json_path=$.login,exa_regex=^({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.login,exa_regex=^({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$'] |
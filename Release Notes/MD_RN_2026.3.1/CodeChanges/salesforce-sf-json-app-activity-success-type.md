# Code Changes for salesforce-sf-json-app-activity-success-type (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'dest_email_address', 'domain', 'email_address', 'full_name', 'time', 'user'] |
| added_regex_field | dest_email_address |  | ['exa_json_path=$.ToAddress,exa_regex=({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|;]+\.[^\]\s"\\,\|;]+)'] |
| added_regex_field | email_address |  | ['exa_json_path=$.CreatedBy.Email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)', 'exa_json_path=$.LastModifiedBy.Email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)'] |
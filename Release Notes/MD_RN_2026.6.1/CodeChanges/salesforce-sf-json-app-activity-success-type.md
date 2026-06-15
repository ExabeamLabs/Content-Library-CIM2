# Code Changes for salesforce-sf-json-app-activity-success-type (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['exa_json_path=$.ToAddress,exa_regex=({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|;]+\.[^\]\s"\\,\|;]+)'] |
| edit_regex_field | email_address |  | ['exa_json_path=$.CreatedBy.Email,exa_regex=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)', 'exa_json_path=$.LastModifiedBy.Email,exa_regex=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)'] |
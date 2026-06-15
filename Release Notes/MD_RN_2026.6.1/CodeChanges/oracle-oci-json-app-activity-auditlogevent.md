# Code Changes for oracle-oci-json-app-activity-auditlogevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_json_path=$.data.resourceName,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({resource_name}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | resource_name |  | ['exa_json_path=$.data.resourceName,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({resource_name}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
# Code Changes for oracle-oci-json-app-activity-auditlogevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ssZ"] |
| changed | Conditions |  | ['"additionalDetails":', '"availabilityDomain":', '"compartmentId":', 'oracle'] |
| changed_parsed_fields | N/A |  | ['email_address', 'resource_name', 'src_ip'] |
| added_regex_field | email_address |  | ['exa_json_path=$.data.resourceName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({resource_name}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | resource_name |  | ['exa_json_path=$.data.resourceName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({resource_name}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
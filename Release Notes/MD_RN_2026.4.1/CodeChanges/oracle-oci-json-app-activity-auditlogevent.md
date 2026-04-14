# Code Changes for oracle-oci-json-app-activity-auditlogevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['email_address', 'http_response_code', 'resource_name', 'src_ip'] |
| added_regex_field | http_response_code |  | ['exa_regex="status":"[^\d"]+({http_response_code}\d+)'] |
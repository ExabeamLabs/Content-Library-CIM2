# Code Changes for sophos-ep-json-alert-trigger-success-recoverykeymissingevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'full_name', 'host', 'src_host', 'src_ip', 'src_port', 'user'] |
| added_regex_field | src_host |  | ['exa_json_path=$.location,exa_regex=^({src_host}[\w\-\.]+)$'] |
| removed_attribute | DupFields |  | N/A |
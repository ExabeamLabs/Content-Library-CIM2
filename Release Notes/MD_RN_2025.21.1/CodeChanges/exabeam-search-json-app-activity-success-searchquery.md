# Code Changes for exabeam-search-json-app-activity-success-searchquery (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'email_address', 'email_domain', 'host', 'object', 'operation', 'query', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | query |  | ['query:\s*\[({object}({query}[^]]+))\]'] |
| added_regex_field | object |  | ['query:\s*\[({object}({query}[^]]+))\]'] |
| removed_attribute | DupFields |  | N/A |
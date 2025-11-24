# Code Changes for shibboleth-s-str-endpoint-login-success-saml (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'email_address', 'principal_name', 'relying_party_id', 'request_binding', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | principal_name |  | ['({time}\d{8}T\d{6}Z)\|(|({action}({request_binding}[^\|]+)))\|[^\|]*\|(|({relying_party_id}[^\|]+))\|([^\|]*\|){4}(|({principal_name}[^\|]+))\|'] |
| edit_regex_field | relying_party_id |  | ['({time}\d{8}T\d{6}Z)\|(|({action}({request_binding}[^\|]+)))\|[^\|]*\|(|({relying_party_id}[^\|]+))\|([^\|]*\|){4}(|({principal_name}[^\|]+))\|'] |
| edit_regex_field | request_binding |  | ['({time}\d{8}T\d{6}Z)\|(|({action}({request_binding}[^\|]+)))\|[^\|]*\|(|({relying_party_id}[^\|]+))\|([^\|]*\|){4}(|({principal_name}[^\|]+))\|'] |
| edit_regex_field | time |  | ['({time}\d{8}T\d{6}Z)\|(|({action}({request_binding}[^\|]+)))\|[^\|]*\|(|({relying_party_id}[^\|]+))\|([^\|]*\|){4}(|({principal_name}[^\|]+))\|'] |
| added_regex_field | action |  | ['({time}\d{8}T\d{6}Z)\|(|({action}({request_binding}[^\|]+)))\|[^\|]*\|(|({relying_party_id}[^\|]+))\|([^\|]*\|){4}(|({principal_name}[^\|]+))\|'] |
| removed_attribute | DupFields |  | N/A |
# Code Changes for akamai-guardicore-cef-app-activity-userauth (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['Audit Record', 'CEF:', 'Guardicore|Centra', 'act='] |
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'category', 'email_address', 'event_name', 'request', 'severity', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | severity |  | ['CEF:\d+\|([^\|]+\|){5}(Unknown|({severity}[^\|]+))'] |
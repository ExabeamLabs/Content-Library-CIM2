# Code Changes for cisco-ucm-kv-configuration-modify-success-generalconfigurationupdate (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| COULD_NOT_COMPARE | TimeFormat | MMM dd yyyy hh:mm:ss a | ['MMM dd yyyy HH:mm:ss a', 'MMM dd yyyy HH:mm:ss.SSS z'] |
| changed_parsed_fields | N/A | ['additional_info', 'app', 'email_address', 'email_domain', 'object', 'operation', 'result', 'src_ip', 'src_port', 'target', 'time', 'user'] | ['additional_info', 'app', 'audit_category', 'email_address', 'email_domain', 'object', 'operation', 'result', 'src_ip', 'src_port', 'target', 'time', 'user'] |
| edit_regex_field | time | ['\s({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+\s+(AM|PM|am|pm))'] | ['\s({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+(\s+(AM|PM|am|pm)|\.\d+\s\w+))'] |
| added_regex_field | audit_category | [] | ['AuditCategory\s*=({audit_category}[^\]]+)'] |
| changed | Conditions | ['EventType =GeneralConfigurationUpdate', '[ AuditDetails ='] | [' %UC_AUDITLOG-', '=GeneralConfigurationUpdate', 'EventType', '[ AuditDetails ='] |
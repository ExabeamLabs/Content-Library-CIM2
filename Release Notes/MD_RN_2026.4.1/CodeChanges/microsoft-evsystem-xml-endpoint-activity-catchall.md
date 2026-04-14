# Code Changes for microsoft-evsystem-xml-endpoint-activity-catchall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'client_name', 'email_address', 'error_code', 'event_code', 'event_id', 'event_name', 'full_name', 'host', 'process_guid', 'process_id', 'provider_name', 'result', 'result_code', 'run_level', 'sub_category', 'tenant_id', 'time', 'user', 'user_sid'] |
| added_regex_field | tenant_id |  | ['\bTenantId=({tenant_id}[^\s,=.<]+)'] |
# Code Changes for microsoft-evpowershell-xml-endpoint-activity-success-eventid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'client_name', 'error_code', 'event_code', 'event_id', 'event_name', 'host', 'process_guid', 'process_id', 'provider_name', 'result', 'result_code', 'run_level', 'sub_category', 'tenant_id', 'time', 'user_sid'] |
| added_regex_field | tenant_id |  | ['\bTenantId=({tenant_id}[^\s,=.<]+)'] |
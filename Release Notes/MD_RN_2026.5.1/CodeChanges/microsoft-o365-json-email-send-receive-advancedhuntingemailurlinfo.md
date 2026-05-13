# Code Changes for microsoft-o365-json-email-send-receive-advancedhuntingemailurlinfo (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_name', 'message_id', 'tenant_id', 'time', 'url', 'web_domain'] |
| added_regex_field | tenant_id |  | ['"(?i:tenantid)":"({tenant_id}[^"]+)'] |
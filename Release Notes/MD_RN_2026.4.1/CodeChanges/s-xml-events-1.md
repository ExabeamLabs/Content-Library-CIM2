# Code Changes for s-xml-events-1 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app_protocol', 'audit_subcategory', 'channel', 'endpoint', 'error_code', 'event_code', 'failure_reason', 'location_information', 'proxy_server', 'relying_party', 'result', 'run_level', 'server', 'time', 'user_agent'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |
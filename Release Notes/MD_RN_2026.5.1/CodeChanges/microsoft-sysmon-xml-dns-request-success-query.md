# Code Changes for microsoft-sysmon-xml-dns-request-success-query (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dns_query', 'dns_response', 'event_code', 'host', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'run_level', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |
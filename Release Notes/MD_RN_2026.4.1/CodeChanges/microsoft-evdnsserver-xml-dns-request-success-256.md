# Code Changes for microsoft-evdnsserver-xml-dns-request-success-256 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes', 'channel', 'dest_ip', 'dest_port', 'dns_query', 'dns_query_flags', 'dns_query_type', 'event_code', 'host', 'process_id', 'query_id', 'run_level', 'src_ip', 'src_port', 'thread_id', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |
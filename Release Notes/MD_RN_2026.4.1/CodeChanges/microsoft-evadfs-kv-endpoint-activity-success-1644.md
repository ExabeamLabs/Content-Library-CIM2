# Code Changes for microsoft-evadfs-kv-endpoint-activity-success-1644 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['attribute_selection', 'attributes_preventing_optimization', 'channel', 'clean_pages_modified', 'dirty_pages_modified', 'domain', 'event_code', 'event_name', 'filter', 'host', 'pages_preread_from_disk', 'pages_read_from_disk', 'pages_referenced', 'returned_entries', 'search_scope', 'search_time', 'server_controls', 'src_ip', 'src_port', 'time', 'used_indexes', 'user', 'user_upn', 'valid_entries'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<\/Channel>'] |
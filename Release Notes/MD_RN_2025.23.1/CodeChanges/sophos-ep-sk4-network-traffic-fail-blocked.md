# Code Changes for sophos-ep-sk4-network-traffic-fail-blocked (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'domain', 'event_name', 'full_name', 'host', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | src_host |  | ['"location":"({src_host}[\w\-.]+)"'] |
| removed_attribute | DupFields |  | N/A |
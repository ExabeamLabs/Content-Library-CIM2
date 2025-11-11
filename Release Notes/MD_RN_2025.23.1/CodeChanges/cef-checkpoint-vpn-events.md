# Code Changes for cef-checkpoint-vpn-events (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'event_name', 'host', 'src_country_code', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | event_name |  | ['\WAction:\s*({event_name}[^;]+)'] |
| removed_attribute | DupFields |  | N/A |
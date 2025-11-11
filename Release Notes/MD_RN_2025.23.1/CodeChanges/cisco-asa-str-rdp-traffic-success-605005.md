# Code Changes for cisco-asa-str-rdp-traffic-success-605005 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth', 'dest_ip', 'dest_port', 'domain', 'event_code', 'host', 'priority', 'protocol', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | protocol |  | ['Login permitted from .+? to .+?/({protocol}.+?) for user'] |
| removed_attribute | DupFields |  | N/A |
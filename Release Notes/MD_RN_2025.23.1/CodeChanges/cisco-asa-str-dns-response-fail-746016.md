# Code Changes for cisco-asa-str-dns-response-fail-746016 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dns_query', 'dns_response', 'event_code', 'event_name', 'failure_reason', 'host', 'priority', 'result_reason', 'time'] |
| added_regex_field | failure_reason |  | [',\s*reason\s*:\s*(UNKNOWN|({failure_reason}.+?))\s*($|\w+=|\'|")'] |
| removed_attribute | DupFields |  | N/A |
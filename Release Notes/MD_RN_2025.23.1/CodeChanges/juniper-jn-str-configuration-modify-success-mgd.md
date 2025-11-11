# Code Changes for juniper-jn-str-configuration-modify-success-mgd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'host', 'operation', 'time', 'user'] |
| added_regex_field | dest_host |  | ['({dest_host}\S+)\s+mgd\s'] |
| removed_attribute | DupFields |  | N/A |
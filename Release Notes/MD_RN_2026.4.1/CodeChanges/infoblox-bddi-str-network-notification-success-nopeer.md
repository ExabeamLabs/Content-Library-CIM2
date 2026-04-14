# Code Changes for infoblox-bddi-str-network-notification-success-nopeer (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['T\d+:[^\s]+\s+({host}[\w.-]+)\s*', '\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s+({src_ip}[a-fA-F\d.:]+?)\s+({additional_info}[^~]+?)\s*$'] |
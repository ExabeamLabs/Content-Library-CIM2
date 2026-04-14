# Code Changes for vmware-esxi-str-endpoint-activity-vmkernel (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['T\d+:[^\s]+\s+({host}[\w.-]+)\s+({event_code}[^:]+?)(\[\d+\])?:\s+({additional_info}[^\$]+?)\s*$', '\s*({host}[\w.-]+)\s*vmkernel:'] |
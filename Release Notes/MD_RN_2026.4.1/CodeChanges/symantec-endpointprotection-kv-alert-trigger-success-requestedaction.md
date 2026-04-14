# Code Changes for symantec-endpointprotection-kv-alert-trigger-success-requestedaction (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['Computer name:\s*(?:0+|({host}[^,]+?)),'] |
| edit_regex_field | src_host |  | ['Computer name:\s*(?:0+|({src_host}[^,]+?)),'] |
# Code Changes for sophos-ep-json-alert-trigger-success-applicationblocked (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | src_host |  | ['"dhost":\s*"({src_host}[^"]+)', '"location":"({src_host}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |
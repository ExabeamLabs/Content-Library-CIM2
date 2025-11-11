# Code Changes for sophos-ep-sk4-alert-trigger-success-savdisable (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['"location":"({src_host}({host}((\d{1,3}\.){3}\d{1,3}|({=src_host}[\w\-.]+))))"'] |
| edit_regex_field | src_host |  | ['"location":"({src_host}({host}((\d{1,3}\.){3}\d{1,3}|({=src_host}[\w\-.]+))))"'] |
| removed_attribute | DupFields |  | N/A |
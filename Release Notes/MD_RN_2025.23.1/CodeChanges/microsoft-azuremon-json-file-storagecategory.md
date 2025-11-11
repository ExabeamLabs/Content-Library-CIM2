# Code Changes for microsoft-azuremon-json-file-storagecategory (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | location |  | ['"location"+:\s*"+({location}({region}[^"]+))"', '"location":"({location}[^"]+)'] |
| edit_regex_field | region |  | ['"location"+:\s*"+({location}({region}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |
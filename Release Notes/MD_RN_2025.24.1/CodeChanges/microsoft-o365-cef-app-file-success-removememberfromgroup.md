# Code Changes for microsoft-o365-cef-app-file-success-removememberfromgroup (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | target |  | ['"Target":\[[^\]]+?"Type"\s*:1,\s*"ID":\s*"({target}[^"]+)', '"targetResources":(?:(?!modifiedProperties)[^}])+?"displayName":"({target}[^"]+)"'] |
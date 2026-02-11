# Code Changes for cisco-umbrella-json-dns-response-success-identities (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | categories |  | ['"categories":\[({categories}"?({category}[^,;"\']+)"?[^\]]+)', 'exa_regex="Categories"*:"*({categories}"?({category}[^,;"\']+)"?[^\]]*?)"'] |
| edit_regex_field | category |  | ['"categories":\[({categories}"?({category}[^,;"\']+)"?[^\]]+)', 'exa_regex="Categories"*:"*({categories}"?({category}[^,;"\']+)"?[^\]]*?)"'] |
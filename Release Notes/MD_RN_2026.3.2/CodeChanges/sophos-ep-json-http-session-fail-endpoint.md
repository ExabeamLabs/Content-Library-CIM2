# Code Changes for sophos-ep-json-http-session-fail-endpoint (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | additional_info |  | ['exa_json_path=$.name,exa_regex=(n\/a|[^"]*? at \\'({additional_info}({malware_url}[^"\\']+)))', 'exa_regex="name":\s*"({additional_info}[^"]+)"'] |
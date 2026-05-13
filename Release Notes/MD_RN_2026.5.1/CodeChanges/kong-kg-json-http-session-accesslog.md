# Code Changes for kong-kg-json-http-session-accesslog (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_json_path=$.request.headers[\'client-header\'],exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|>]+))'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.request.headers[\'client-header\'],exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|>]+))'] |
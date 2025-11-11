# Code Changes for okta-amfa-json-app-login-fail-userlogintookta (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user |  | ['"type":\s\"User\"\,\s+\"alternateId\"\:\s\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)', 'exa_json_path=$.actor.alternateId,exa_regex=(?:(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s"]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({=user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'exa_regex="type":\s\"User\"\,\s+\"alternateId\"\:\s\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| removed_attribute | DupFields |  | N/A |
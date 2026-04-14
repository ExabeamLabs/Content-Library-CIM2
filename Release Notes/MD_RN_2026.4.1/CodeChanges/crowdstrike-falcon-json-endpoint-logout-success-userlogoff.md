# Code Changes for crowdstrike-falcon-json-endpoint-logout-success-userlogoff (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"UserPrincipal":"({email_address}([A-Za-z0-9]+[!#$%&\'+\-\.\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!(local))(?<!(loc))(?<!(localdomain))"', 'exa_json_path=$.UserPrincipal,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\-\.\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!(local))(?<!(loc))(?<!(localdomain))', 'exa_regex="UserPrincipal":"({email_address}([A-Za-z0-9]+[!#$%&\'+\-\.\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!(local))(?<!(loc))(?<!(localdomain))"'] |
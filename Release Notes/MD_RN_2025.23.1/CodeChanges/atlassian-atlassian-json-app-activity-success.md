# Code Changes for atlassian-atlassian-json-app-activity-success (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['email_address', 'email_domain'] |
| added_regex_field | email_address |  | ['exa_json_path=$..attributes.actor.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))'] |
| added_regex_field | email_domain |  | ['exa_json_path=$..attributes.actor.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))'] |
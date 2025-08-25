# Code Changes for microsoft-sentinel-json-group-member-add-success-addmembertogroup (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['email_address', 'email_domain'] | ['dest_email_address', 'email_address', 'email_domain'] |
| edit_regex_field | email_address | ['exa_json_path=$.ActivityInsights.UserAdded,exa_field_name=dest_email_address({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))', 'exa_json_path=$.UserPrincipalName,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] | ['exa_json_path=$.UserPrincipalName,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| added_regex_field | dest_email_address | [] | ['exa_json_path=$.ActivityInsights.UserAdded,exa_regex=({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
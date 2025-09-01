# Code Changes for cisco-ie-str-email-from (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'email_address', 'email_domain', 'time'] |
| edit_regex_field | email_address |  | ['(F|f)rom[:\']*.+?<({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))>'] |
| removed_regex_field | src_email_domain |  | [] |
| added_regex_field | email_domain |  | ['(F|f)rom[:\']*.+?<({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))>'] |
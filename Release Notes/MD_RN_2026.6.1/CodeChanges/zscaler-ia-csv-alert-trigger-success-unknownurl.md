# Code Changes for zscaler-ia-csv-alert-trigger-success-unknownurl (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))",("[^"]*",){10}"Unknown URL"'] |
| edit_regex_field | email_domain |  | ['"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))",("[^"]*",){10}"Unknown URL"'] |
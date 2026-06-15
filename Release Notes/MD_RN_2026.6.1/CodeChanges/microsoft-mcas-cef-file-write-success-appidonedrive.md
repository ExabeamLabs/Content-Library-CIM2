# Code Changes for microsoft-mcas-cef-file-write-success-appidonedrive (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['Add user to group in site:\s?user\s?({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s?to group\s?({group_name}[^=]+)\s?suser'] |
| edit_regex_field | dest_email_domain |  | ['Add user to group in site:\s?user\s?({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s?to group\s?({group_name}[^=]+)\s?suser'] |
| edit_regex_field | group_name |  | ['Add user to group in site:\s?user\s?({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s?to group\s?({group_name}[^=]+)\s?suser'] |
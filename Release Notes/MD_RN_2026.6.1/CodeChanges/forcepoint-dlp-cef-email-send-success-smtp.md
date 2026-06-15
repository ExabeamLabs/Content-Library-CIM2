# Code Changes for forcepoint-dlp-cef-email-send-success-smtp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['\sduser=({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | dest_email_domain |  | ['\sduser=({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,;\|]+))'] |
# Code Changes for symantec-esc-str-email-sender (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | alert_id |  | ['\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|SENDER\|(?:<>|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| edit_regex_field | email_address |  | ['\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|SENDER\|(?:<>|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| edit_regex_field | email_domain |  | ['\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|SENDER\|(?:<>|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| edit_regex_field | time |  | ['\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|SENDER\|(?:<>|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
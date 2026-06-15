# Code Changes for symantec-esc-str-email-recipient (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | alert_id |  | ['\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|ORCPTS\|({email_recipients}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+).*?)\s*$'] |
| edit_regex_field | email_recipients |  | ['\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|ORCPTS\|({email_recipients}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+).*?)\s*$'] |
| edit_regex_field | time |  | ['\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|ORCPTS\|({email_recipients}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+).*?)\s*$'] |
# Code Changes for microsoft-o365-json-email-send-receive-internentmessageid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['"Recipients":\[?"({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"?\]?'] |
| edit_regex_field | email_address |  | ['"P1Sender":"((([^@]+?\\=)+)?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({email_user}[^"]+))"', '"P2Sender":"((([^@]+?\\=)+)?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({email_user}[^"]+))"'] |
| edit_regex_field | email_recipients |  | ['"Recipients":\[?"({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"?\]?'] |
| edit_regex_field | email_user |  | ['"P1Sender":"((([^@]+?\\=)+)?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({email_user}[^"]+))"', '"P2Sender":"((([^@]+?\\=)+)?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({email_user}[^"]+))"'] |
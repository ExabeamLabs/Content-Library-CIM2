# Code Changes for cisco-ie-str-email-bytesfrom (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | bytes |  | ['({bytes}\d+) bytes from <({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)>'] |
| edit_regex_field | email_address |  | ['({bytes}\d+) bytes from <({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)>'] |
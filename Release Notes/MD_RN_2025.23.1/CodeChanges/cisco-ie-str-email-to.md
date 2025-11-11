# Code Changes for cisco-ie-str-email-to (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'dest_email_address', 'dest_email_domain', 'message_id', 'time'] |
| edit_regex_field | alert_id |  | ['MID ({message_id}({alert_id}\d+)) .*? To: <({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))>'] |
| edit_regex_field | dest_email_address |  | ['MID ({message_id}({alert_id}\d+)) .*? To: <({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))>'] |
| edit_regex_field | dest_email_domain |  | ['MID ({message_id}({alert_id}\d+)) .*? To: <({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))>'] |
| added_regex_field | message_id |  | ['MID ({message_id}({alert_id}\d+)) .*? To: <({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))>'] |
| removed_attribute | DupFields |  | N/A |
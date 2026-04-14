# Code Changes for cisco-secureemail-json-email-send-receive-esa (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'bytes', 'dest_email_address', 'direction', 'email_address', 'email_subject', 'message_id', 'policy_name', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | dest_email_address |  | ['\sduser=({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)'] |
| removed_regex_field | dest_email_domain |  | [] |
| edit_regex_field | email_address |  | ['\ssuser=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)'] |
| removed_regex_field | email_domain |  | [] |
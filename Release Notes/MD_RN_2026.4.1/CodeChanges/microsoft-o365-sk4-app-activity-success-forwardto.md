# Code Changes for microsoft-o365-sk4-app-activity-success-forwardto (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'correlation_id', 'dest_email_address', 'dest_email_domain', 'email_address', 'email_domain', 'email_recipients', 'filter_key_words', 'host', 'object', 'operation', 'result', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | email_recipients |  | ['"SentTo[^\}]+Value":"(smtp:)?({email_recipients}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"', 'Value":"(smtp:)?({email_recipients}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"[^\}]+"SentTo"'] |
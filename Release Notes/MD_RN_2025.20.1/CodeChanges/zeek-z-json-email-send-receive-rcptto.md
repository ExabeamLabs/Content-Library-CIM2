# Code Changes for zeek-z-json-email-send-receive-rcptto (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['connection_id', 'dest_email_address', 'dest_email_domain', 'dest_ip', 'dest_port', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'helo', 'protocol', 'src_ip', 'src_port', 'time', 'user_agent'] |
| removed_regex_field | domain |  | [] |
| removed_regex_field | user |  | [] |
| added_regex_field | email_address |  | ['"mailfrom":\s*"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))', 'exa_regex="mailfrom":\s*"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| added_regex_field | email_domain |  | ['"mailfrom":\s*"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))', 'exa_regex="mailfrom":\s*"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
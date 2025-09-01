# Code Changes for mimecast-seg-cef-app-activity-success-messageviewlogs (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'dest_email_address', 'dest_email_domain', 'email_address', 'email_domain', 'email_subject', 'log_source', 'operation', 'resource', 'result', 'target', 'time'] |
| edit_regex_field | email_address |  | ['"from":"\s*(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)(?<!loc)))"', '"viewer":"\s*(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)(?<!loc)))"'] |
| edit_regex_field | email_domain |  | ['"from":"\s*(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)(?<!loc)))"', '"viewer":"\s*(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)(?<!loc)))"'] |
| removed_regex_field | src_email_address |  | [] |
| removed_regex_field | src_email_domain |  | [] |
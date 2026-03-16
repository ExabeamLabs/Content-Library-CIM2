# Code Changes for json-google-email-activity (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'dest_email_address', 'dest_email_domain', 'email_address'] |
| edit_regex_field | email_address |  | ['exa_json_path=$.message_info.source.address,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)'] |
| removed_regex_field | email_domain |  | [] |
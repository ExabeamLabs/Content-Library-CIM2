# Code Changes for microsoft-defenderep-json-mailbox-item-delete-success-emailpostdeliveryeventsdelete (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['exa_json_path=$..RecipientEmailAddress,exa_regex=({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | dest_email_domain |  | ['exa_json_path=$..RecipientEmailAddress,exa_regex=({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
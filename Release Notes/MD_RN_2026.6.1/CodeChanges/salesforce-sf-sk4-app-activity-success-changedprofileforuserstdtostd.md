# Code Changes for salesforce-sf-sk4-app-activity-success-changedprofileforuserstdtostd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\Wsuser=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(\s+\w+=|\s*$)'] |
| edit_regex_field | email_domain |  | ['\Wsuser=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(\s+\w+=|\s*$)'] |
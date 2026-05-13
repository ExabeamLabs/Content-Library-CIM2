# Code Changes for salesforce-sf-cef-file-upload-success-cloud-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['CreatedBy\.Username\\?=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|;]+\.[^\]\s"\\,\|;]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?);)'] |
| edit_regex_field | user |  | ['CreatedBy\.Username\\?=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|;]+\.[^\]\s"\\,\|;]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?);)'] |
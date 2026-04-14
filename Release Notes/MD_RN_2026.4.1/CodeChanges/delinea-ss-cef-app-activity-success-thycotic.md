# Code Changes for delinea-ss-cef-app-activity-success-thycotic (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'dest_user', 'domain', 'email_address', 'host', 'object', 'operation', 'resource', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | dest_user |  | ['Account Name:\s*({dest_user}[\w\.\-]{1,40}\$?)'] |
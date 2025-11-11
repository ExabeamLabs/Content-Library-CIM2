# Code Changes for microsoft-windows-xml-peripheral-storage-activity-success-devicewasdisable (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'device_class', 'device_description', 'device_id', 'device_pid', 'device_vid', 'domain', 'event_code', 'event_name', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^\<]+))<\/Data>'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<\/Data>'] |
| added_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^\<]+))<\/Data>'] |
| added_regex_field | src_user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<\/Data>'] |
| removed_attribute | DupFields |  | N/A |
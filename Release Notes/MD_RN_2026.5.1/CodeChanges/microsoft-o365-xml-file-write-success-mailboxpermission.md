# Code Changes for microsoft-o365-xml-file-write-success-mailboxpermission (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'channel', 'domain', 'full_name', 'host', 'object', 'operation', 'resource', 'result', 'run_level', 'time', 'user'] |
| added_regex_field | channel |  | ['<Channel>({channel}.+?)<\/Channel>'] |
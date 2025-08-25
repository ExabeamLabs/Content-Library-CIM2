# Code Changes for microsoft-evsecurity-xml-endpoint-start-4608 (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | additional_info | ['<Message>({additional_info}[^<]+?)\s*<'] | ['<Data>({additional_info}[^<]+)<', '<Message>({additional_info}[^<]+?)\s*<'] |
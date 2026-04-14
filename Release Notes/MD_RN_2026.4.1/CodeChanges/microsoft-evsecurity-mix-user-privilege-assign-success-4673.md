# Code Changes for microsoft-evsecurity-mix-user-privilege-assign-success-4673 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'dest_host', 'dest_ip', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object_server', 'privileges', 'process_dir', 'process_name', 'process_path', 'result', 'service_name', 'time', 'user'] |
| edit_regex_field | event_code |  | ['({event_code}4673)', '<EventID>({event_code}\d+)<\/EventID>'] |
| edit_regex_field | host |  | ['"(Hostname|MachineName|computer_name)":"({host}[\w\-.]*)', '({result}(((audit|success|failure)( |_)(success|audit|failure))|information))\s*(\s|\t|,|#\d+|<[^>]+>)\s*(4673|({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-\.]+))))\s*(\s|\t|,|#\d+|<[^>]+>)\s*', ':\d{2}\s+({host}[\w.-]+)\s+((audit|success|failure)( |_)(success|audit|failure))\s+4673', '<Computer>({host}[\w\-\.]+)<\/Computer>', '<\d+>\w+\s*\d+\s*\d+:\d+:\d+\s+(am\s+|pm\s+)?(::ffff:)?({dest_host}({host}[\w\-.]+))\s', 'Computer(Name)?\s*(=|:)\s*({host}[\w\-.]+)'] |
| edit_regex_field | time |  | ['"TimeCreated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', '"TimeCreated":"[\\\/]*Date\(({time}\d{13})', '"\@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3}Z)"', '({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(AM|PM))', '({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+4673', '<TimeCreated SystemTime="({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.\d{1,9}Z)"\/>"', 'TimeGenerated=({time}\d{10})'] |
| added_regex_field | additional_info |  | ['<EventData><Data>({additional_info}[^\<]+)<\/Data><\/EventData>'] |
| added_regex_field | channel |  | ['Channel"?(:|>)"?({channel}[^"<]+)'] |